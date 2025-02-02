#Feedback-tool-for-essay-using-BERT-and-T5 

# Simplified Essay Feedback Tool (for presentation purposes)

def score_essay(essay_text):
    # In a real application, you would use a model like BERT here.
    # For this demo, we'll just assign a random score.
    # Replace this with your actual scoring logic when you have it working.
    # This simplistic scoring is only for demo purposes.
    words = essay_text.split()
    word_count = len(words)

    if word_count < 50:
        score = "Poor"  # Example
    elif word_count < 150:
        score = "Average" # Example
    else:
      score = "Good" # Example

    return score

def generate_feedback(essay_text, score):
    # In a real application, you would use a model like T5 here.
    # For this demo, we'll provide some placeholder feedback.
    # Replace this with your actual feedback generation when you have it.
    # This simplistic feedback is only for demo purposes.
    feedback_templates = {
        "Poor": "The essay needs significant improvement in terms of content, structure, and clarity.",
        "Average": "The essay is a good start, but it could benefit from more details, examples, and a stronger conclusion.",
        "Good": "The essay demonstrates a good understanding of the topic and presents well-supported arguments."
    }
    feedback = feedback_templates.get(score, "Feedback not available for this score.") # Default message

    return feedback


# Example Usage (replace with your actual essay)
essay = """This is a sample essay for the presentation.  It's a short one, just for demonstration. I want to show how my project works."""


predicted_score = score_essay(essay)
feedback = generate_feedback(essay, predicted_score)

print(f"Predicted Score: {predicted_score}")
print(f"Feedback: {feedback}")


