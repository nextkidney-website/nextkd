# NEXTKIDNEY MPESA Integration (Node.js Production)

## How to set up

1. Copy this folder to your server.
2. Install dependencies:

```
npm install
```

3. Create a `.env` file and fill your MPESA credentials:

```
CONSUMER_KEY=your_consumer_key
CONSUMER_SECRET=your_consumer_secret
SHORT_CODE=your_shortcode
PASSKEY=your_passkey
CALLBACK_URL=https://yourdomain.com/callback
```

4. Start the server:

```
npm start
```

5. From your frontend, make a POST request to `/pay` with JSON body:

```
{
  "phone": "2547XXXXXXXX",
  "amount": 1000
}
```

6. The customer will receive an STK push on their phone to approve.

---

## Callback

MPESA will send a POST to `/callback` with payment result. You can modify this to update your order status.

---

## Note

- Make sure your server uses **HTTPS** for MPESA to work.
- Replace `yourdomain.com` with your actual domain.
