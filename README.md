# Angi QA Review Assistant · Homeowner Experience Team

This is an internal-only QA coaching assistant designed for CX Team Leads (like Marcus) at Angi to review agent responses, rate them against standard rubrics, flag legal risks, and generate constructive feedback.

## Features

1. **Angi Branding & Light Theme**: Built using a modern, accessible light theme styled around Angi's official Coral Red (`#FF6153`) brand colors, complete with a crisp, custom-drawn inline SVG Angi heart wordmark.
2. **Onboarding Guide**: Features a built-in visual 3-step guide for first-time users directly on the empty results panel state to explain the review workflow.
3. **Hidden API Key Integration**: Removed visible API key fields from the UI to protect keys. The app automatically runs on the default provided Groq key, with support for customizable key overrides saved via `localStorage` (via the browser console).
4. **Context-Aware Evaluation**: Evaluates the agent's draft response *specifically* against the customer's complaint/context and standard company policy rules.
5. **Interactive Case Templates**: Selectable via a dropdown menu, including:
   - **Sample 1: Contractor No-Show (Lost Wages & Threat)**: Double no-show frustrations, lost wages, and public posting threats.
   - **Sample 2: Refund Dispute (Overcommitted Refund)**: A scenario containing unauthorized refund promises violating financial caps.
   - **Sample 3: Property Damage (Unacknowledged Damage & Risk)**: A scenario showing high legal risk where the agent leaves a customer to handle damage alone.

## Getting Started

To run the application locally:

1. **Start the local server** (already running in the background on port `8000`):
   ```bash
   python3 -m http.server 8000
   ```
2. **Access the application**:
   Open [http://localhost:8000](http://localhost:8000) in your web browser.

3. **Use the Application**:
   - The Groq API key is pre-filled invisibly. (To override, run `localStorage.setItem('groq_api_key', 'YOUR_KEY')` in your browser console).
   - Use the **Select case template** dropdown to load one of the 3 pre-configured scenarios, or choose **New / Custom Case** to write a fresh evaluation.
   - Click **Run QA review →** to generate the analysis.
