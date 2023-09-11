# Create-a-URL-shortening-service-that-converts-long-URLs-into-short-
import random
import string

url_dict = {}

def generate_short_url():
    characters = string.ascii_letters + string.digits
    return ''.join(random.choice(characters) for _ in range(6))

def shorten_url(long_url):
    short_url = generate_short_url()
    url_dict[short_url] = long_url
    return short_url

def main():
    long_url = input("Enter the long URL: ")
    short_url = shorten_url(long_url)
    print(f"Shortened URL: http://yourdomain.com/{short_url}")

if __name__ == "__main__":
    main()
