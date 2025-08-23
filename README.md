# GreenTrack: Empowering Global Environmental Action

## Project Overview

GreenTrack is a web-based application designed to empower individuals and communities to contribute to global environmental action. It provides tools for reporting environmental issues, tracking tree planting activities, and fostering a community of eco-conscious users. The platform aims to make environmental stewardship accessible and engaging through features like gamification and interactive mapping.

## Features

- **Interactive Map:** Visualize reported environmental issues and tree planting locations worldwide.
- **Tree Planting Tracking:** Record and track your tree planting efforts, contributing to global reforestation data.
- **Environmental Reporting:** Easily report environmental concerns, such as illegal dumping or pollution, with location and photo details.
- **Community Engagement:** Connect with other users, share stories, and participate in discussions.
- **Gamification:** Earn experience points (XP) and level up as you contribute to environmental initiatives.
- **Leaderboard:** See how your contributions stack up against other users.
- **News and Updates:** Stay informed about environmental news and project updates.
- **User Profiles:** Manage your personal information and view your environmental impact.

## Installation

To set up GreenTrack on your local machine, follow these steps:

1.  **Prerequisites:**
    *   Apache Web Server
    *   PHP (with `php-mysql` extension)
    *   MySQL Database

2.  **Clone the Repository:**
    ```bash
    git clone <repository_url>
    cd greentrack
    ```
    *(Note: Replace `<repository_url>` with the actual repository URL if available.)*

3.  **Unzip the project files:**
    If you received the project as a zip file, unzip it to your desired directory (e.g., `/home/ubuntu/greentrack`).
    ```bash
    unzip greentrack.zip -d /home/ubuntu/greentrack
    ```

4.  **Database Setup:**
    *   Create a MySQL database for GreenTrack.
    *   Import the provided SQL schema (e.g., `greentrack/sql/gamification_tables.sql`) into your database.
    *   Update the database connection details in `greentrack/includes/db.php` to match your database configuration.

5.  **Apache Configuration:**
    *   Create a new Apache virtual host configuration file (e.g., `/etc/apache2/sites-available/greentrack.conf`):

    ```apache
    <VirtualHost *:80>
        ServerAdmin webmaster@localhost
        DocumentRoot /home/ubuntu/greentrack/greentrack/public_html
        <Directory /home/ubuntu/greentrack/greentrack/public_html>
            Options Indexes FollowSymLinks
            AllowOverride All
            Require all granted
        </Directory>
        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined
    </VirtualHost>
    ```

    *   Enable the new site and disable the default Apache site:

    ```bash
    sudo a2ensite greentrack.conf
    sudo a2dissite 000-default.conf
    ```

    *   Ensure Apache has read and execute permissions for the project directory:

    ```bash
    sudo chmod -R 755 /home/ubuntu/greentrack
    sudo chmod o+x /home/ubuntu
    ```

    *   Restart Apache to apply the changes:

    ```bash
    sudo systemctl restart apache2
    ```

## Usage

Once the application is installed and running, you can access it through your web browser at `http://localhost/` (or the domain configured in your Apache virtual host).

-   **Home Page:** Provides an overview of recent activities, global statistics, and how the platform works.
-   **Map:** Explore environmental data on an interactive map.
-   **Plant:** Record your tree planting activities.
-   **Report:** Submit reports on environmental issues.
-   **Leaderboard:** View top contributors and their XP.
-   **Recommended Locations:** Discover areas suggested for environmental action.
-   **Stories:** Read and share personal stories related to environmental efforts.

## Interface Previews

Here are some previews of the GreenTrack application interface:

### Home Page

![Home Page Preview](images/greentrack_index.png)

The home page provides a welcoming introduction to GreenTrack, highlighting its mission and key functionalities. It features sections for recent activity, global statistics, and a clear call to action for new users.

### Map Page

![Map Page Preview](images/greentrack_map.png)

The map page offers an interactive visualization of environmental data, allowing users to explore reported issues and tree planting locations across the globe. It provides a geographical context to environmental efforts.

### Plant Trees Page

![Plant Trees Page Preview](images/greentrack_plant_trees.png)

This page allows users to record their tree planting activities. It includes fields for species, quantity, date, and a description, enabling users to track their contributions to reforestation efforts.

## Contributing

We welcome contributions to GreenTrack! If you'd like to contribute, please fork the repository and submit a pull request with your changes. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.

## Contact

For any inquiries or support, please contact [Your Email/Contact Info Here].



