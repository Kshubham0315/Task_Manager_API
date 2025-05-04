# Task_Manager_API
Ek backend API jo user authentication (/auth) aur task management (/task) ke liye endpoints provide karta hai.
🔍 Detailed Breakdown:
✅ 1. Middleware Setup:
express.json()
→ Request body ko JSON format mein parse karta hai. Required for POST/PUT data.

express-session
→ Server-side session handle karta hai. Sessions ko cookie ke through track karta hai.

cookie-parser
→ Cookies ko parse karta hai, so you can access them via req.cookies.

✅ 2. Routes Setup:
js
Copy code
import authRoute from "./routes/auth.route.js";
import taskRoute from "./routes/task.route.js";
/auth route ka kaam hoga: Login / Register / Logout

/task route ka kaam hoga: Task create / update / delete / list

✅ 3. Default Route:
js
Copy code
app.get("/", (req, res) => {
    res.send("Welcome to Task Manager API📗");
});
Jab koi browser ya client root URL (e.g., http://localhost:8080/) par jaata hai, yeh welcome message return hota hai.

✅ 4. Server Initialization:
js
Copy code
app.listen(PORT, () => {
  console.log(`Server is running on PORT ${PORT}`);
});
Port 8080 par server run hota hai.

📦 Summary:
Yeh project ek backend API app hai jo:

Sessions aur cookies ke sath login system banata hai,

Task management ke endpoints provide karta hai,

Express ke middleware se request processing karta hai.
