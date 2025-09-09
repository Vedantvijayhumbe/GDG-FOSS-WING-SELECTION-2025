# Streamlit 

Streamlit is an open-source Python library that helps us create interactive web applications directly from Python scripts.

advantages of streamlit : 
1. Easy to use → You only need Python knowledge; no HTML, CSS, or JavaScript.

2. Quick prototyping → Turn scripts into shareable apps in minutes.

3. Interactive widgets → Supports buttons, sliders, file uploads, checkboxes, and more.

4. Real-time updates → Automatically refreshes the app when the code changes.

5. Open-source & free → whoosh , anyone can use and contribute.

6. Deployment is easy → Host apps easily on Streamlit Cloud or any other platform like Vercel . 

7. decent enough UI by default 

8. Lightweight & fast → Ideal for small to medium apps and dashboards. optimised for ML since already the models are heavy to render , having lightweight framework boosts web performance . 


# why streamlit is better than flask for ML/data applications : 

Streamlit is better suited for data applications because it lets developers build interactive dashboards and ML demos using only Python, without needing HTML, CSS, or JavaScript. It integrates seamlessly with libraries like Pandas, Matplotlib, and Plotly, and includes built-in widgets such as sliders and file uploaders, making development faster and simpler.

Flask, on the other hand, is a general-purpose web framework ideal for complex, production-grade web apps. But for rapid prototyping and data-focused projects, Streamlit offers a cleaner and more efficient solution.

# Auto Refreshment in streamlit 

Streamlit automatically reruns the entire script whenever:

A user interacts with a widget (e.g., slider, button, input).

The source code is saved/modified.

This ensures the UI always reflects the latest state. To avoid re-executing heavy tasks on every refresh, Streamlit provides caching decorators like @st.cache_data and @st.cache_resource.

Example: A slider movement triggers a rerun, updating outputs in real time without manual reload.

# basic workflow 

Install Streamlit --> pip install streamlit.

Write a Python script with Streamlit functions in .py sort of file 

Run streamlit run app.py and see it in the browser. you can edit it too and see live changes coz of auto refreshment 

# open source history of Streamlit 

1. 2018 : first release on github . basic widgets 
2. 2019 : Added support for file uploads (st.file_uploader).
3. 2020 : introduced custom components for third-party integrations . Improved caching (@st.cache) for faster performance.
4. 2021 : streamlit cloud for deployement . no other services needed now to deploy streamlit apps . 
5. 2022 : enhanced caching and made it lightweight 
6. 2023 : support for multipage apps , enhanced widgets . 





