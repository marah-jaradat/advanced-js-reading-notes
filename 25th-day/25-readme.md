# 18-May-2022- 25th class reading notes:

## <Login /> and <Auth /> :

### **What is Cookie?**

A cookie is a piece of data (key-value pairs) that is stored on the user’s computer by the web browser while browsing a site. Cookies are designed to be a reliable mechanism for websites to remember stateful information or to record the user’s browsing activity or verify the user identity.

#### **Their purpose**

React & Share uses cookies to compose analytics and reports for its clients. React & Share analyzes the quality and usage of the content on the client’s website and offers a channel for the end users to give feedback. Cookies cannot be used to identify users.

#### **What data is saved**

React & Share saves a browser specific random-generated id as a first party cookie.

**The following data can be associated with the cookie:**
1. Timestamp
2. Type of device and browser used
3. Visited pages on the site
4. Time spent on a page
5. From which URL the user browsed to a page
6. What reactions the user gave on a page
7. Where the user shared a page
8. What feedback the user left on a page
9. Period of validity
React & Share saves cookies for 30 days after which they are automatically removed.

**Third parties**
React & Share uses all data only for the client. Cookies are saved as first party cookies, i.e. they can only be used on client’s site and domain. Other third parties cannot utilize the cookies or any data associated with them. React & Share will not sell or distribute any data to third parties.

#### **Install**

    $ npm install react-cookies --save


**.plugToRequest(req, res): unplug()**
Load the user cookies so you can do server-rendering and match the same result.
Also send back to the user the new cookies.
Work with connect or express.js by using the cookieParser middleware first.
Use const unplug = plugToRequest(req, res) just before your renderToString.

Returns unplug() function so it stops setting cookies on the response.

.**setRawCookie(cookies)**
Load the user cookies so you can do server-rendering and match the same result.
Use setRawCookie(headers.cookie) just before your renderToString.
Make sure it is the raw string from the request headers.

### **<CookiesProvider />**

Set the user cookies
On the server, the cookies props must be set using req.universalCookies or new Cookie(cookieHeader)

**useCookies([dependencies])**
Access and modify cookies using React hooks.

    const [cookies, setCookie, removeCookie] = useCookies(['cookie-name']);


**dependencies (optional)**
Let you optionally specify a list of cookie names your component depend on or that should trigger a re-render. If unspecified, it will render on every cookie change.

**cookies**
Javascript object with all your cookies. The key is the cookie name.

    setCookie(name, value, [options])

Set a cookie value

- name (string): cookie name
- value (string|object): save the value and stringify the object if needed
- options (object): Support all the cookie options from RFC 6265
    - path (string): cookie path, use / as the path if you want your cookie to be accessible on all pages
    - expires (Date): absolute expiration date for the cookie
    - maxAge (number): relative max age of the cookie from when the client receives it in seconds
    - domain (string): domain for the cookie (sub.domain.com or .allsubdomains.com)
    - secure (boolean): Is only accessible through HTTPS?
    - httpOnly (boolean): Can only the server access the cookie? Note: You cannot get or set httpOnly cookies from the browser, only the server.
    - sameSite (boolean|none|lax|strict): Strict or Lax enforcement
  
[react-cookie](https://www.npmjs.com/package/react-cookie)

### **What is Role-Based Access Control (RBAC)?** 

Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.

Employees are only allowed to access the information necessary to effectively perform their job duties. Access can be based on several factors, such as authority, responsibility, and job competency. In addition, access to computer resources can be limited to specific tasks such as the ability to view, create, or modify a file.

As a result, lower-level employees usually do not have access to sensitive data if they do not need it to fulfill their responsibilities. This is especially helpful if you have many employees and use third-parties and contractors that make it difficult to closely monitor network access. Using RBAC will help in securing your company’s sensitive data and important applications.

#### **EXAMPLES OF ROLE-BASED ACCESS CONTROL**

Through RBAC, you can control what end-users can do at both broad and granular levels. You can designate whether the user is an administrator, a specialist user, or an end-user, and align roles and access permissions with your employees’ positions in the organization. Permissions are allocated only with enough access as needed for employees to do their jobs.

What if an end-user's job changes? You may need to manually assign their role to another user, or you can also assign roles to a role group or use a role assignment policy to add or remove members of a role group.

**Some of the designations in an RBAC tool can include:**

- Management role scope – it limits what objects the role group is allowed to manage.
- Management role group – you can add and remove members.
- Management role – these are the types of tasks that can be performed by a specific role group.
- Management role assignment – this links a role to a role group.
 
By adding a user to a role group, the user has access to all the roles in that group. If they are removed, access becomes restricted. Users may also be assigned to multiple groups in the event they need temporary access to certain data or programs and then removed once the project is complete.

**Other options for user access may include:**

- Primary – the primary contact for a specific account or role.
- Billing – access for one end-user to the billing account.
- Technical – assigned to users that perform technical tasks.
- Administrative – access for users that perform administrative tasks.

#### **BENEFITS OF RBAC**
Managing and auditing network access is essential to information security. Access can and should be granted on a need-to-know basis. With hundreds or thousands of employees, security is more easily maintained by limiting unnecessary access to sensitive information based on each user’s established role within the organization. Other advantages include:

1. Reducing administrative work and IT support.
2. Maximizing operational efficiency.
3. Improving compliance.

[RBAC](https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more)

[gh-pages](https://marah-jaradat.github.io/advanced-js-reading-notes/)

[My-repo](https://github.com/marah-jaradat/advanced-js-reading-notes/blob/gh-pages/25th-day/25-readme.md)
