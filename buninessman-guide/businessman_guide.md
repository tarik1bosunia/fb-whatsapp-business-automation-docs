# Businessman's Guide to Platform Integration

## Introduction

Welcome to the Businessman's Guide for integrating your social media platforms with our service. This guide provides step-by-step instructions to connect your Facebook and WhatsApp accounts, enabling you to streamline your customer communications and enhance engagement.

By following this guide, you will be able to:

- **Automate** customer interactions on Facebook and WhatsApp.
- **Centralize** your messaging workflows.
- **Leverage** our platform's features to grow your business.

## Table of Contents

- [Facebook Integration](#facebook-integration)
  - [Step 1: Create a Facebook App](#step-1-create-a-facebook-app)
  - [Step 2: Obtain App ID and App Secret](#step-2-obtain-app-id-and-app-secret)
  - [Step 3: Configure Settings on Our Platform](#step-3-configure-settings-on-our-platform)
  - [Step 4: Set App ID and App Secret](#step-4-set-app-id-and-app-secret)
  - [Step 5: Generate a Short-Lived Access Token](#step-5-generate-a-short-lived-access-token)
  - [Step 6: Set the Short-Lived Access Token](#step-6-set-the-short-lived-access-token)
  - [Step 7: Create and Set a Facebook Verify Token](#step-7-create-and-set-a-facebook-verify-token)
  - [Step 8: Connect Your Account](#step-8-connect-your-account)
- [Verify Webhook and Permissions](#verify-webhook-and-permissions)
  - [Step 1: Go to the Webhooks Page](#step-1-go-to-the-webhooks-page)
  - [Step 2: Configure Webhook](#step-2-configure-webhook)
  - [Step 3: Verify and Save](#step-3-verify-and-save)
  - [Step 4: Subscribe to Permissions](#step-4-subscribe-to-permissions)
- [WhatsApp Integration](#whatsapp-integration)
- [Troubleshooting](#troubleshooting)

---

## Facebook Integration

This section will walk you through integrating your Facebook Page with our platform.

<details>
<summary>Step 1: Create a Facebook App</summary>

First, you need to create a Facebook App. You can do this by visiting the [Facebook for Developers portal](https://developers.facebook.com/apps/creation/).

- Click on the **Create App** button.
- Provide an **App name** and your **App contact email**.

![Creating a Facebook App](./images/create_fb_app_001.png)
![App creation process](./images/create_fb_app_002.png)
![App creation process](./images/create_fb_app_003.png)
![App creation process](./images/create_fb_app_004.png)
![App creation process](./images/create_fb_app_005.png)
![App creation process](./images/create_fb_app_006.png)
![App creation process](./images/create_fb_app_007.png)
![App creation process](./images/create_fb_app_008.png)
![App creation process](./images/create_fb_app_009.png)
![App creation process](./images/create_fb_app_010.png)
![App creation process](./images/create_fb_app_011.png)

</details>

<details>
<summary>Step 2: Obtain App ID and App Secret</summary>

Once your app is created, you will need to get your **App ID** and **App Secret**.

![Finding App ID and Secret](./images/fb_app_id_secret_get_001.png)
![Finding App ID and Secret](./images/fb_app_id_secret_get_002.png)
![Finding App ID and Secret](./images/fb_app_id_secret_get_003.png)
![Finding App ID and Secret](./images/fb_app_id_secret_get_004.png)
![Finding App ID and Secret](./images/fb_app_id_secret_get_005.png)

</details>

<details>
<summary>Step 3: Configure Settings on Our Platform</summary>

Navigate to our settings page to continue the integration: [https://smartchatbot.click/settings](https://smartchatbot.click/settings). Then, click on the **Platform Integrations** tab.

![Platform Integrations Tab](./images/facebook_integrations_start.png)
</details>

<details>
<summary>Step 4: Set App ID and App Secret</summary>

Enter the **App ID** and **App Secret** you obtained from the Facebook Developer portal into the respective fields on our platform.

![Setting App ID and Secret](./images/fb_app_id_secret_secret_set_001.png)
![Setting App ID and Secret](./images/fb_app_id_secret_secret_set_002.png)
![Setting App ID and Secret](./images/fb_app_id_secret_secret_set_003.png)
![Setting App ID and Secret](./images/fb_app_id_secret_secret_set_004.png)
![Setting App ID and Secret](./images/fb_app_id_secret_secret_set_005.png)

</details>

<details>
<summary>Step 5: Generate a Short-Lived Access Token</summary>

You will need to generate a short-lived access token from the **Graph API Explorer**.

- Select your app.
- Grant the necessary permissions (e.g., `pages_show_list`, `pages_read_engagement`, `pages_manage_metadata`, `pages_messaging`).
- Generate the token.

![Generating Access Token](./images/short_live_access_token_get_001.png)
![Generating Access Token](./images/short_live_access_token_get_002.png)
![Generating Access Token](./images/short_live_access_token_get_003.png)
![Generating Access Token](./images/short_live_access_token_get_004.png)
![Generating Access Token](./images/short_live_access_token_get_005.png)
![Generating Access Token](./images/short_live_access_token_get_006.png)
![Generating Access Token](./images/short_live_access_token_get_007.png)
![Generating Access Token](./images/short_live_access_token_get_008.png)
![Generating Access Token](./images/short_live_access_token_get_009.png)
![Generating Access Token](./images/short_live_access_token_get_010.png)
![Generating Access Token](./images/short_live_access_token_get_011.png)
![Generating Access Token](./images/short_live_access_token_get_012.png)

</details>

<details>
<summary>Step 6: Set the Short-Lived Access Token</summary>

Copy the generated token and paste it into the designated field on our platform.

![Setting Short-Lived Token](./images/short_live_access_token_set_001.png)
</details>

<details>
<summary>Step 7: Create and Set a Facebook Verify Token</summary>

Create a unique and secure **Verify Token**. It should be more than 20 characters long.

![Setting Verify Token](./images/set_fb_verify_token_001.png)
![Confirming Verify Token](./images/set_fb_verify_token_002.png)
</details>

<details>
<summary>Step 8: Connect Your Account</summary>

Click the **Connect** button to finalize the connection.

![Connection Success](./images/facebook_integration_success.png)
</details>

---

## Verify Webhook and Permissions

A webhook enables real-time communication between Facebook and our platform.

<details>
<summary>Step 1: Go to the Webhooks Page</summary>

In your Facebook App settings, navigate to the **Webhooks** page.

![Webhooks Page](./images/webhook_facebook_01.png)
![Webhooks Page](./images/webhook_facebook_02.png)

</details>

<details>
<summary>Step 2: Configure Webhook</summary>

- Select the **Pages** tab.
- Enter the **Callback URL**: `https://api.smartchatbot.click/api/messaging/webhook/messenger/` (ensure the trailing `/` is included).
- Enter the same **Verify Token** you created earlier.

![Configuring Webhook](./images/webhook_facebook_03.png)
</details>

<details>
<summary>Step 3: Verify and Save</summary>

Click **Verify and Save**.

![Verify and Save](./images/webhook_facebook_04.png)
![Verify and Save](./images/webhook_facebook_05.png)
![Verify and Save](./images/webhook_facebook_06.png)
</details>

<details>
<summary>Step 4: Subscribe to Permissions</summary>

Subscribe to the required permissions under the **Pages** tab.

![Subscribing to Permissions](./images/webhook_facebook_07.png)
![Subscribing to Permissions](./images/webhook_facebook_08.png)
![Subscribing to Permissions](./images/permission_and_feature_01.png)
</details>

Congratulations! Your Facebook integration is now complete.

---

## WhatsApp Integration

<details>
<summary>WhatsApp Integration Guide</summary>

Integrating your WhatsApp Business Account allows you to manage customer conversations directly through our platform. This section will guide you through connecting your WhatsApp Business Account.

Our WhatsApp integration is designed to be simple and straightforward. To get started, you will need a WhatsApp Business Account and an approved phone number.

**Key Benefits of WhatsApp Integration:**

*   **Direct Customer Engagement:** Communicate with your customers on their preferred messaging app.
*   **Automated Notifications:** Send order confirmations, shipping updates, and appointment reminders.
*   **24/7 Customer Support:** Use chatbots to answer frequently asked questions and resolve issues instantly.
*   **Personalized Marketing:** Deliver targeted promotions and special offers to your audience.

**Coming Soon:**

We are currently finalizing the documentation for WhatsApp integration. Please check back soon for a detailed, step-by-step guide.

![WhatsApp Integration Start](./images/whatsapp_integration_start.png)
</details>

---

## Troubleshooting

<details>
<summary>Common Issues and Solutions</summary>

If you encounter any issues during the integration process, refer to the common problems and solutions below.

**Common Issues:**

*   **Invalid App ID or App Secret:**
    *   **Solution:** Double-check that you have copied the correct App ID and App Secret from your Facebook Developer account. Ensure there are no extra spaces or characters.

*   **Incorrect Callback URL:**
    *   **Solution:** Verify that the Callback URL is entered correctly in your webhook settings. It must be `https://api.smartchatbot.click/api/messaging/webhook/messenger/` and include the trailing `/`.

*   **Permissions Not Granted:**
    *   **Solution:** Ensure that you have granted all the required permissions in your Facebook App settings. These include `pages_show_list`, `pages_read_engagement`, `pages_manage_metadata`, and `pages_messaging`.

*   **Webhook Verification Failed:**
    *   **Solution:** Confirm that the Verify Token on our platform matches the one you entered in your Facebook App's webhook settings. They must be identical.

If you continue to experience problems, please contact our support team for assistance.
</details>
