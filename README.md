# Install the library first:
# pip install googletrans==4.0.0-rc1

from googletrans import Translator

def translate_text(text, src_lang='en', dest_lang='fr'):
    translator = Translator()
    translation = translator.translate(text, src=src_lang, dest=dest_lang)
    return translation.text

# Example usage
if __name__ == "__main__":
    input_text = "Hello, how are you?"
    translated = translate_text(input_text, src_lang='en', dest_lang='es')
    print(f"Original: {input_text}")
    print(f"Translated: {translated}")

# pip install deep-translator

from deep_translator import GoogleTranslator

result = GoogleTranslator(source='auto', target='de').translate("Good morning!")
print(result)  # Output: Guten Morgen!
