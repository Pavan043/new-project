# The translation & audio heartbeat
translator.source = "auto"
translator.target = lang_map[target_language]
translated = translator.translate(input_text)
# Logic to play audio instantly in browser
tts = gTTS(text=translated, lang=target_code)
fp =BytesIO()tts.write_to_fp(fp)
b64 = base64.b64encode(fp.getvalue()).decode()
st.markdown(f'<audio autoplay="true" src="data:audio/mp3;base64,{b64}">', unsafe_allow_html=True)
