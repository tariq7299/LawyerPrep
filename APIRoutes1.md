
1. **Identity Bounded Context**
   - `POST /api/v1/office/{id}/identity/register` (Register a new user, either a lawyer or a client)
   - `POST /api/v1/office/{id}/identity/login` (Authenticate a user)
   - `GET /api/v1/office/{id}/identity/profile` (Retrieve user profile information)
   - `PUT /api/v1/office/{id}/identity/profile` (Update user profile information)

2. **Office info Bound**
   - `GET /api/v1/office/{id}/info` (List available lawyers)
   - `PUT /api/v1/office/{id}/info` (List available lawyers)
   - `POST /api/v1/office/{id}/info` (List available lawyers)

2. **News and Announcements Bounded Context**
   -  GET /api/v1/office/{id}/news (Get a list of news and announcements for the office)
   -  GET /api/v1/office/{id}/news/{newsId} (Get details of a specific news or announcement)
   -  POST /api/v1/office/{id}/news (Create a new news or announcement for the office)
   -  PUT /api/v1/office/{id}/news/{newsId} (Update an existing news or announcement)
   -  DELETE /api/v1/office/{id}/news/{newsId} (Delete a news or announcement)

2. **Lawyers Bounded Context**

   - `GET /api/v1/office/{id}/lawyers` (List available lawyers)
   - `GET /api/v1/office/{id}/lawyers/{lawyerId}` (Retrieve details of a specific lawyer)
   - `PUT /api/v1/office/{id}/lawyers/{lawyerId}` (Update lawyer profile information)

   - `GET /api/v1/office/{id}/lawyers/{lawyerId}/services/` view all services (his obligations)

   - `GET /api/v1/office/{id}/lawyers/{lawyerId}/services/lawsuits/` view all services (appointments-consultations-lawsuits)
   - `GET /api/v1/office/{id}/lawyers/{lawyerId}/services/appointments/` view all services (appointments-consultations-lawsuits)
   - `GET /api/v1/office/{id}/lawyers/{lawyerId}/services/consultations/` view all services (appointments-consultations-lawsuits)

   - `GET /api/v1/office/{id}/lawyers/{lawyerId}/services/lawsuits/{id}` view all services (appointments-consultations-lawsuits)
   - `GET /api/v1/office/{id}/lawyers/{lawyerId}/services/appointments/{id}` view all services (appointments-consultations-lawsuits)
   - `GET /api/v1/office/{id}/lawyers/{lawyerId}/services/consultations/{id}` view all services (appointments-consultations-lawsuits)

   - `GET /api/v1/office/{id}/lawyers/{lawyerId}/services/lawsuits/{id}/documents` view all services (appointments-consultations-lawsuits)
   - `GET /api/v1/office/{id}/lawyers/{lawyerId}/services/appointments/{id}/documents` view all services (appointments-consultations-lawsuits)
   - `GET /api/v1/office/{id}/lawyers/{lawyerId}/services/consultations/{id}/documents` view all services (appointments-consultations-lawsuits)

   - `GET /api/v1/office/{id}/lawyers/{lawyerId}/services/lawsuits/{id}` view all services (appointments-consultations-lawsuits)
   - `GET /api/v1/office/{id}/lawyers/{lawyerId}/services/lawsuits/court-appearneces` view all services  to view for example the court appearnces you can filter lawsutits by the with court appearnce
   - `GET /api/v1/office/{id}/lawyers/{lawyerId}/services/lawsuits/{id}/court-appearneces` view all services  to view for example the court appearnces you can filter lawsutits by the with court appearnce


   - `PUT /api/v1/office/{id}/lawyers/{lawyerId}` (Update lawyer profile information) // This needs more thinking as the lawyer can't create an account ! only office manager can create an account
   - `PUT /api/v1/office/{id}/lawyers/{lawyerId}` (Update lawyer profile information)

   - `/`
   

3. **Clients Bounded Context**
   - `GET /api/v1/office/{id}/clients/lawyers` (Search and filter lawyers based on criteria)
   - `POST /api/v1/office/{id}/clients/services/appointments` (Request a legal consultation)
   - `GET /api/v1/office/{id}/clients/services/appointments` (List a client's scheduled consultations)
   - `POST /api/v1/office/{id}/clients/services/consultations` (Request a legal consultation)
   - `GET /api/v1/office/{id}/clients/services/consultations` (List a client's scheduled consultations)
   - `POST /api/v1/office/{id}/clients/services/lawsuits` (Initiate a new lawsuit)
   - `GET /api/v1/office/{id}/clients/services/lawsuits` (List a client's ongoing lawsuits)


4. **Services Bounded Context**
   - `GET /api/v1/office/{id}/services/consultations/`
   - `GET /api/v1/office/{id}/services/appointments/`
   - `GET /api/v1/office/{id}/services/lawsuits/`
   - `GET /api/v1/office/{id}/services/consultations/{serviceId}`
   - `GET /api/v1/office/{id}/services/appointments/{serviceId}`
   - `GET /api/v1/office/{id}/services/lawsuits/{serviceId}`
   - `PUT /api/v1/office/{id}/services/consultations/{serviceId}`
   - `PUT /api/v1/office/{id}/services/appointments/{serviceId}`
   - `PUT /api/v1/office/{id}/services/lawsuits/{serviceId}`
   - `GET /api/v1/office/{id}/services/consultations/{serviceId}/documents`
   - `GET /api/v1/office/{id}/services/appointments/{serviceId}/documents`
   - `GET /api/v1/office/{id}/services/lawsuits/{serviceId}/documents`
   - `POST /api/v1/office/{id}/services/consultations/{serviceId}/documents`
   - `POST /api/v1/office/{id}/services/appointments/{serviceId}/documents`
   - `POST /api/v1/office/{id}/services/lawsuits/{serviceId}/documents`
   - `PUT /api/v1/office/{id}/services/consultations/{serviceId}/documents`
   - `PUT /api/v1/office/{id}/services/appointments/{serviceId}/documents`
   - `PUT /api/v1/office/{id}/services/lawsuits/{serviceId}/documents`

6. **Billing Bounded Context**
   - `POST /api/v1/office/{id}/billing/payments` (Process a payment)
   - `GET /api/v1/office/{id}/billing/invoices` (List invoices for a user)
   - `GET /api/v1/office/{id}/billing/subscriptions` (List active subscriptions for a user)

7. **Notifications Bounded Context**
   - `POST /api/v1/office/{id}/notifications` (Send a notification to a user)
   - `GET /api/v1/office/{id}/notifications` (Retrieve notifications for a user)

8. **Chat Bounded Context** ------
   - `GET /api/v1/office/{id}/chat/conversations{conversationId}/{userA}` get all message in a chat for a user
   - `GET /api/v1/office/{id}/chat/conversations{conversationId}/{userA}/{userB}` get all message in a chat for two users