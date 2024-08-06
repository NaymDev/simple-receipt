# 📜 Receipt Viewer

Welcome to the **Receipt Viewer** repository! This project provides a simple and convenient way to display receipts through a static webpage hosted on GitHub Pages. You can use this tool to visualize receipt data by passing it via URL parameters.

## 📌 Why This Project?

In today’s world, managing receipts can be a hassle. This project aims to simplify the process by allowing you to generate and view receipt data through a straightforward URL. It's designed for ease of use and can be embedded or accessed in various contexts where a quick receipt view is needed.

### 🚀 Features:
- **Easy Integration**: Embed or share URLs with receipt data.
- **Simple Setup**: Hosted statically on GitHub Pages, so no server configuration required.
- **Flexibility**: Use anywhere you can provide a URL, making it ideal for quick checks and sharing.

## 🛠️ How to Use

1. **Prepare Your Data**: Create your receipt data in the form of a JSON array. For example:
    ```json
    [["members", 10, 0.2], ["Express", "10%"]]
    ```

2. **Encode the Data**: Convert the JSON array into a URL-encoded string. Here’s how you can do it in Python:
    ```python
    import json
    import urllib.parse

    items = [["members", 10, 0.2], ["Express", "10%"]]
    json_string = json.dumps(items)
    encoded_items = urllib.parse.quote(json_string)
    print(f"?items={encoded_items}")
    ```

3. **Access the Webpage**: Use the encoded data in the URL to access your receipt:
    ```
   https://naymdev.github.io/simple-receipt/?items=%5B%5B%22members%22%2C10%2C0.2%5D%2C%5B%22Express%22%2C%2210%25%22%5D%5D
    ```

Replace `your-github-username` with your actual GitHub username.

## ⚠️ Important Note

This tool is designed for convenience and visualization purposes only. **It is not secure** and should not be used for sensitive information or critical applications. The data is processed client-side and is visible in the URL, so avoid using it for private or sensitive receipts.

## 🌐 Live Demo

You can try out the demo [here](https://naymdev.github.io/simple-receipt/). Just append your encoded receipt data to the URL to see it in action.

## 🧩 Customization

Feel free to fork this repository and customize the webpage to better fit your needs. Contributions and improvements are always welcome!

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

Thank you for checking out **Receipt Viewer**!

---

*Hosted on GitHub Pages for a seamless and accessible experience.*
