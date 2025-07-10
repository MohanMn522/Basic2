import spacy

# Load medium English model with word vectors
nlp = spacy.load("en_core_web_md")

def check_similarity(text1, text2, threshold=0.85):
    """
    Compare two texts and return a similarity score.
    """
    doc1 = nlp(text1)
    doc2 = nlp(text2)
    similarity = doc1.similarity(doc2)
   
    print(f"Similarity Score: {similarity:.2f}")
   
    if similarity >= threshold:
        print("⚠️ Potential plagiarism detected.")
    else:
        print("✅ Content appears original.")

# Example usage
original_text = """
The internet is flooded with content, making it challenging to spot plagiarism.
Our AI-powered tool helps news organizations detect copied content quickly.
"""

suspect_text = """
With so much content online, it's tough to identify plagiarism.
This AI tool enables media to find stolen material fast.
"""

check_similarity(original_text, suspect_text)

