# 🚀 Livewire FlyonUI Starter Kit

A modern, feature-rich starter kit for building dynamic web applications with Laravel Livewire and FlyonUI components. This starter kit provides everything you need to quickly bootstrap your next project with a beautiful, responsive UI and powerful real-time functionality.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Laravel](https://img.shields.io/badge/Laravel-11.x-FF2D20?logo=laravel)](https://laravel.com)
[![Livewire](https://img.shields.io/badge/Livewire-3.x-4E56A6?logo=livewire)](https://livewire.laravel.com)
[![FlyonUI](https://img.shields.io/badge/FlyonUI-Latest-06B6D4?logo=tailwindcss)](https://flyonui.com)

## ✨ Features

- **🎨 Modern UI Components**: Pre-built FlyonUI components for rapid development
- **⚡ Real-time Interactions**: Powered by Laravel Livewire for seamless user experiences
- **📱 Responsive Design**: Mobile-first approach with Tailwind CSS integration
- **🔧 Developer Experience**: Hot reload, debugging tools, and optimized workflows
- **🚀 Performance Optimized**: Built with best practices for speed and scalability
- **🔐 Authentication Ready**: Pre-configured authentication system
- **📦 Component Library**: Reusable Livewire components for common use cases
- **🎯 TypeScript Support**: Optional TypeScript integration for enhanced development

## 🛠️ Tech Stack

- **Backend**: Laravel 11.x
- **Frontend Framework**: Laravel Livewire 3.x
- **UI Components**: FlyonUI
- **Styling**: Tailwind CSS 3.x
- **Build Tool**: Vite
- **Database**: MySQL/PostgreSQL/SQLite
- **Cache**: Redis (optional)
- **Testing**: PHPUnit, Pest

## 📋 Requirements

- PHP 8.2 or higher
- Composer 2.x
- Node.js 18.x or higher
- NPM or Yarn
- MySQL 8.0+ / PostgreSQL 13+ / SQLite 3.8+

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/emmieIO/livewire-flyonui-starter.git
cd livewire-flyonui-starter
```

### 2. Install Dependencies

```bash
# Install PHP dependencies
composer install

# Install Node.js dependencies
npm install
```

### 3. Environment Setup

```bash
# Copy environment file
cp .env.example .env

# Generate application key
php artisan key:generate

# Configure your database in .env file
# DB_CONNECTION=mysql
# DB_HOST=127.0.0.1
# DB_PORT=3306
# DB_DATABASE=your_database
# DB_USERNAME=your_username
# DB_PASSWORD=your_password
```

### 4. Database Setup

```bash
# Run migrations
php artisan migrate

# (Optional) Seed the database
php artisan db:seed
```

### 5. Build Assets

```bash
# Development
npm run dev

# Production
npm run build
```

### 6. Start the Application

```bash
php artisan serve
```

Visit `http://localhost:8000` to see your application running!

## 📚 Usage

### Creating Livewire Components

```bash
# Create a new Livewire component
php artisan make:livewire UserProfile

# Create a component with a custom view
php artisan make:livewire UserProfile --view=components.user-profile
```

### Using FlyonUI Components

```blade
<!-- Example: Using FlyonUI Button -->
<button class="btn btn-primary">
    Click me!
</button>

<!-- Example: Using FlyonUI Card -->
<div class="card">
    <div class="card-body">
        <h2 class="card-title">Card Title</h2>
        <p>Card content goes here.</p>
        <div class="card-actions justify-end">
            <button class="btn btn-primary">Action</button>
        </div>
    </div>
</div>
```

### Livewire Integration Example

```php
<?php

namespace App\Livewire;

use Livewire\Component;

class Counter extends Component
{
    public $count = 0;

    public function increment()
    {
        $this->count++;
    }

    public function decrement()
    {
        $this->count--;
    }

    public function render()
    {
        return view('livewire.counter');
    }
}
```

```blade
{{-- resources/views/livewire/counter.blade.php --}}
<div class="card w-96 bg-base-100 shadow-xl">
    <div class="card-body">
        <h2 class="card-title">Counter: {{ $count }}</h2>
        <div class="card-actions justify-end">
            <button class="btn btn-secondary" wire:click="decrement">-</button>
            <button class="btn btn-primary" wire:click="increment">+</button>
        </div>
    </div>
</div>
```

## 🏗️ Project Structure

```
├── app/
│   ├── Http/Controllers/
│   ├── Livewire/          # Livewire components
│   ├── Models/
│   └── ...
├── resources/
│   ├── css/
│   │   └── app.css        # Tailwind CSS + custom styles
│   ├── js/
│   │   └── app.js         # Frontend JavaScript
│   └── views/
│       ├── components/    # Blade components
│       ├── livewire/      # Livewire views
│       └── layouts/       # Layout files
├── public/
├── routes/
├── database/
├── tests/
└── ...
```

## 🎨 Customization

### Extending FlyonUI Themes

```css
/* resources/css/app.css */
@import 'tailwindcss/base';
@import 'tailwindcss/components';
@import 'tailwindcss/utilities';

/* Custom FlyonUI theme extensions */
:root {
  --primary: 259 94% 51%;
  --secondary: 314 100% 47%;
}
```

### Adding Custom Components

1. Create Livewire component: `php artisan make:livewire CustomComponent`
2. Design with FlyonUI classes in the blade template
3. Add any required JavaScript interactions
4. Register in your layout or pages as needed

## 🧪 Testing

```bash
# Run all tests
php artisan test

# Run specific test suite
php artisan test --testsuite=Feature

# Run with coverage
php artisan test --coverage
```

## 🚀 Deployment

### Production Build

```bash
# Install production dependencies
composer install --optimize-autoloader --no-dev

# Build assets for production
npm run build

# Optimize Laravel
php artisan config:cache
php artisan route:cache
php artisan view:cache
```

### Environment Configuration

```bash
# Set production environment
APP_ENV=production
APP_DEBUG=false

# Configure production database and cache
# Set up proper file permissions
# Configure web server (Apache/Nginx)
```

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

### Development Workflow

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make your changes
4. Run tests: `php artisan test`
5. Commit changes: `git commit -m 'Add amazing feature'`
6. Push to branch: `git push origin feature/amazing-feature`
7. Open a Pull Request

### Coding Standards

- Follow PSR-12 coding standards for PHP
- Use Laravel best practices
- Write meaningful commit messages
- Include tests for new features
- Update documentation as needed

## 📖 Documentation

- [Laravel Documentation](https://laravel.com/docs)
- [Livewire Documentation](https://livewire.laravel.com/docs)
- [FlyonUI Documentation](https://flyonui.com/docs)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

## 🐛 Issues & Support

If you encounter any issues or need support:

1. Check the [Issues](https://github.com/emmieIO/livewire-flyonui-starter/issues) page
2. Search existing issues before creating a new one
3. Provide detailed information about your environment and the problem
4. Include steps to reproduce the issue

## 📝 Changelog

See [CHANGELOG.md](CHANGELOG.md) for details about changes in each version.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Laravel Team](https://laravel.com/team) for the amazing framework
- [Livewire Team](https://github.com/livewire/livewire) for reactive components
- [FlyonUI Team](https://flyonui.com) for beautiful UI components
- [Tailwind CSS Team](https://tailwindcss.com) for the utility-first CSS framework

---

<p align="center">
  <strong>Built with ❤️ by <a href="https://github.com/emmieIO">emmieIO</a></strong>
</p>

<p align="center">
  <a href="https://github.com/emmieIO/livewire-flyonui-starter/stargazers">⭐ Star this repo if you find it helpful!</a>
</p>
