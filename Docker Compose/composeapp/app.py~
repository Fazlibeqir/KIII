from flask import Flask
from redis import Redis

app = Flask(__name__)
redis = Redis(host="redis", port=6379, decode_responses=True)

@app.route('/')
def hello():
    redis.incr('hits')
    hits = redis.get('hits')
    return f'Hello Docker Book reader! I have been seen {hits} times'

if __name__ == "__main__":
    app.run(host="0.0.0.0", debug=True)
