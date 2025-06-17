import openai 
import os

# Use environment variable for security *****
openai.api_key = "XXXXXXXXXXX"

#4 faqs for testing
#questions posed to personnel at work
#about insurance provider / queries concerning table of benefits tob
#datatype- dictionary, consisting of key and value pairs where key is the potential question and value is the prescribed answer in tob

faq = {
    "What are the optical benefits covered at ophthalmologist clinics?": 
        "Optical benefits include specialist visits, optical examinations for obtaining eye glasses or upgrading existing lenses, a pair of lenses (not contact lenses), frame is NOT covered.",

    "What are the dentist benefits?": 
        "Coverage for tooth extraction, temporary & permanent filling, scaling & polishing, amalgam & composite fillings, x-rays, extractions, root canal, consultations & medications for infection only; Excluding cosmetics: preventative cleaning, scaling & polishing, crowns, implants, prostheses, false teeth, panoramic x-rays, orthodontics, temporomandibular joint syndrome, gum disease.",

    "Preventive services, vaccines, and immunizations":
        "Preventive services as stipulated by DHA including initial diabetes screening: every 3 years from age 30, and annually from age 18 for high-risk individuals; Hepatitis B Virus Screening and Treatment: As per DHA guidelines; Cancer Screening & Treatment: As per the guidelines for colorectal, cervical, and breast cancer (LSB Segment); Adult Pneumococcal Conjugate Vaccine: As per DHA guidelines.",

    "What is the Alternative Medicine Cover?": 
        "Includes chiropractor, osteopathy, homeopathy, ayurveda, chiropody, acupuncture, herbal treatment, and podiatry; Covered: Up to AED 5,000 PPPY. OP Co-Insurance: 0%. Payment procedure: On Direct Billing / Reimbursement Basis."
    
}

#integrated ai aids question matching to find accurate queries that coincide with user questions
def find_best_match(user_input):
    question_list = "\n".join(f"- {q}" for q in faq.keys())
    prompt = f"""
You are an AI that matches user questions to the closest FAQ entry.
Here are the available questions:
{question_list}

User question: "{user_input}"

Respond with the most similar question EXACTLY as written above. Do not rephrase or generate a new question.
"""

    response = openai.ChatCompletion.create(model="model=gpt-3.5-turbo",messages=[{"role": "user", "content": prompt}],temperature=0.2,max_tokens=100)

    matched_question = response['choices'][0]['message']['content'].strip()

    #case matching
    for key in faq:
        if matched_question.lower() == key.lower():
            return faq[key]

    return "Sorry, I don't have an answer for that."

#example
if __name__ == "__main__":
    user_query = input("Ask your query: ")
    response = find_best_match(user_query)
    print("\nAnswer:")
    print(response)

