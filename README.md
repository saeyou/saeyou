




def get_response(query):
    url = "https://api.bard.ai/v1/answer"
    params = {"query": query, "bru_mode": "true"}
    response = requests.get(url, params=params)
    return response.json()["answer"]

def main():
    query = input("Enter your query: ")
    response = get_response(query)
    print(response)

if __name__ == "__main__":
    main()
