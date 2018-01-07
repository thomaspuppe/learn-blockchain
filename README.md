# Learn blockchain by building one

Tutorial from https://hackernoon.com/learn-blockchains-by-building-one-117428612f46

    git clone git@github.com:thomaspuppe/learn-blockchain.git
    cd learn-blockchain
    virtualenv -p /usr/bin/python3 venv
    source ./venv/bin/activate
    python --version
    > Python 3.6.3
    pip install Flask requests

**Commands and URLs as reminder**

    python blockchain.py
    python blockchain.py 5001

- http://127.0.0.1:5000/nodes/resolve
- http://127.0.0.1:5001/chain
- http://127.0.0.1:5001/mine

Curl or postman:
    
    curl -X POST -H "Content-Type: application/json" -d '{ "sender": "d4ee26eee15148ee92c6cd394edd974e", "recipient": "someone-other-address", "amount": 5 }' "http://localhost:5001/transactions/new"
  
    curl -X POST -H "Content-Type: application/json" -d '{ "nodes": ["http://127.0.0.1:5001"] }' "http://localhost:5000/nodes/register"
