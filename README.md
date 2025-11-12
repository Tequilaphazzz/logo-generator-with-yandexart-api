# Logo Generator using Yandex-ART API

This project is a logo generator that uses the Yandex-ART API to create images based on text descriptions. The web application, developed using Flask, allows users to specify parameters such as shape, style, and logo description, and generate high-quality images.

## Key Features
- **Yandex-ART API Integration**:
  - Image generation based on text descriptions.
  - Use of cascaded diffusion methods for high-quality detail.
- **Flexible Parameters**:
  - Ability to specify shape, style, and other logo characteristics.
  - Support for various aspect ratios and random values for uniqueness of each image.
- **Ease of Use**:
  - User-friendly web interface with a form for entering parameters.
  - Results are displayed directly on the application page.

## Technologies and Tools
- **Python**: Primary development language.
- **Flask**: Framework for creating web applications.
- **Yandex-ART API**: Generative model for image creation.
- **HTML, CSS, Bootstrap**: For creating the user interface.

## Project Structure
1. **API Configuration**:
   - Created a configuration file `config.py` containing the IAM token and catalog ID.
   - Implemented automatic request processing to the Yandex-ART API.
2. **Core Logic**:
   - The `logo_gen.py` file handles request processing, logo generation, and image saving.
3. **Web Interface**:
   - The `app.py` file contains routes for the Flask application.
   - Data input form is available through the `index.html` HTML template.
4. **Additions**:
   - `static` folder for storing generated images.
   - Automation of IAM token updates through a separate script.

## Installation and Launch
1. **Install dependencies**:
   ```bash
   pip install flask requests
   ```
2. **Configure settings**:
   
   In the `config.py` file, specify your IAM token and catalog ID:
   ```python
   iam_token = "YOUR_IAM_TOKEN"
   catalog_id = "YOUR_CATALOG_ID"
   ```
3. **Run the application**:
   ```bash
   python app.py
   ```
4. **Open in browser**:
   
   Navigate to: `http://127.0.0.1:5000`.

## Usage Example
1. Enter logo parameters (shape, style, description).
2. Click "Generate Logo".
3. Receive the finished image saved in the `static` folder.

## Potential Improvements
- Add visualization of the generation process (loading animation).
- Integrate support for other image generation APIs.
- Optimize request processing and reduce result waiting time.
