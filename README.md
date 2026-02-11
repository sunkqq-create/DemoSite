# DemoSite
# This is a demo for a pricing website.




<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Architectura Web | Enterprise-Grade Tier-Scaled Development</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/cookieconsent@3/build/cookieconsent.min.css">
    <style>
      @keyframes fadeIn {
        from {
          opacity: 0;
          transform: translateY(20px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }
      .fade-in {
        animation: fadeIn 0.6s ease-out;
      }
      @keyframes float {
        0%,
        100% {
          transform: translateY(0px);
        }
        50% {
          transform: translateY(-15px);
        }
      }
      .float-animation {
        animation: float 4s ease-in-out infinite;
      }
      @keyframes gradient {
        0% {
          background-position: 0% 50%;
        }
        50% {
          background-position: 100% 50%;
        }
        100% {
          background-position: 0% 50%;
        }
      }
      .gradient-animate {
        background-size: 200% 200%;
        animation: gradient 8s ease infinite;
      }
      .hidden {
        display: none !important;
      }
      ::-webkit-scrollbar {
        width: 10px;
      }
      ::-webkit-scrollbar-track {
        background: rgba(255, 255, 255, 0.05);
      }
      ::-webkit-scrollbar-thumb {
        background: linear-gradient(180deg, #3b82f6, #8b5cf6);
        border-radius: 5px;
      }
      .glassmorphism {
        background: rgba(255, 255, 255, 0.05);
        backdrop-filter: blur(10px);
        border: 1px solid rgba(255, 255, 255, 0.1);
      }
      .tier-card {
        transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
      }
      .tier-card:hover {
        transform: translateY(-10px) scale(1.02);
      }

      /* Additional styles for mockup content */
      .ripple {
        position: absolute;
        border-radius: 50%;
        background: rgba(255, 255, 255, 0.3);
        transform: scale(0);
        animation: ripple-animation 0.6s linear;
      }

      @keyframes ripple-animation {
        to {
          transform: scale(4);
          opacity: 0;
        }
      }

      .loaded body {
        opacity: 1;
        transition: opacity 0.5s ease;
      }
    </style>
  </head>
  <body
    class="bg-gradient-to-br from-slate-900 via-indigo-900 to-slate-900 min-h-screen text-white"
  >
    <!-- Animated Background -->
    <div class="fixed inset-0 overflow-hidden pointer-events-none">
      <div
        class="absolute top-1/4 left-1/4 w-96 h-96 bg-blue-500/10 rounded-full blur-3xl float-animation"
      ></div>
      <div
        class="absolute top-2/3 right-1/4 w-96 h-96 bg-purple-500/10 rounded-full blur-3xl float-animation"
        style="animation-delay: 2s"
      ></div>
    </div>

    <!-- Sticky CTA -->
    <div class="fixed top-20 right-5 z-50 hidden md:block">
      <button
        onclick="showRequestForm()"
        class="bg-gradient-to-r from-emerald-500 to-teal-500 hover:from-emerald-600 hover:to-teal-600 text-white font-bold py-4 px-8 rounded-full shadow-2xl transition-all duration-300 transform hover:scale-110"
      >
        🚀 Get Started
      </button>
    </div>

    <!-- Mobile CTA -->
    <div
      class="fixed bottom-0 left-0 right-0 bg-gradient-to-r from-emerald-600 to-teal-600 p-4 z-50 md:hidden"
    >
      <button
        onclick="showRequestForm()"
        class="w-full text-white font-bold py-4 rounded-xl"
      >
        🚀 Start Your Project
      </button>
    </div>

    <!-- Navigation -->
    <nav class="glassmorphism sticky top-0 z-40 border-b border-white/10">
      <div
        class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center"
      >
        <div
          onclick="showView('home')"
          class="cursor-pointer flex items-center gap-4"
        >
          <div class="text-4xl">🏗️</div>
          <div>
            <h1
              class="text-3xl font-bold bg-gradient-to-r from-blue-400 via-purple-400 to-pink-400 bg-clip-text text-transparent gradient-animate"
            >
              Architectura Web
            </h1>
            <p class="text-xs text-gray-400">Enterprise Development</p>
          </div>
        </div>
        <div class="hidden md:flex items-center gap-8">
          <button
            onclick="showView('home')"
            class="hover:text-blue-400 transition"
          >
            Home
          </button>
          <button
            onclick="showView('portfolio')"
            class="hover:text-purple-400 transition"
          >
            Portfolio
          </button>
          <button
            onclick="showView('pricing')"
            class="hover:text-emerald-400 transition"
          >
            Pricing
          </button>
          <button
            onclick="showRequestForm()"
            class="bg-gradient-to-r from-blue-600 to-purple-600 px-6 py-2.5 rounded-full font-bold"
          >
            Get Quote
          </button>
        </div>
      </div>
    </nav>

    <!-- HOME VIEW -->
    <div id="homeView" class="relative">
      <div class="max-w-7xl mx-auto px-6 py-24">
        <!-- Hero -->
        <div class="text-center mb-32">
          <div
            class="glassmorphism p-4 rounded-2xl inline-flex items-center gap-4 mb-8"
          >
            <span class="text-3xl">👨‍💻</span>
            <div class="text-left">
              <div class="text-emerald-300 font-bold text-lg">
                Solo Developer Excellence
              </div>
              <div class="text-gray-400 text-sm">
                Tier-Scaled • Enterprise Quality
              </div>
            </div>
          </div>

          <h2 class="text-7xl font-bold mb-8 leading-tight">
            Build
            <span
              class="bg-gradient-to-r from-blue-400 to-purple-600 bg-clip-text text-transparent"
              >Intelligent</span
            >
            Websites<br />
            That
            <span
              class="bg-gradient-to-r from-emerald-400 to-teal-400 bg-clip-text text-transparent"
              >Scale</span
            >
          </h2>

          <p class="text-2xl text-gray-300 mb-12 max-w-4xl mx-auto">
            You get direct access to who is responsible for your website
          </p>

          <div class="flex justify-center gap-6 mb-16">
            <button
              onclick="showView('portfolio')"
              class="bg-gradient-to-r from-blue-600 via-purple-600 to-pink-600 px-10 py-5 rounded-2xl font-bold text-lg hover:scale-105 transition shadow-2xl gradient-animate"
            >
              🎨 Explore Demos
            </button>
            <button
              onclick="showRequestForm()"
              class="glassmorphism px-10 py-5 rounded-2xl font-bold text-lg border-2 border-white/20 hover:bg-white/10 transition"
            >
              💬 Free Consultation
            </button>
          </div>

          <!-- Features -->
          <div class="grid md:grid-cols-4 gap-6 max-w-5xl mx-auto">
            <div class="glassmorphism p-6 rounded-xl">
              <div class="text-4xl mb-2">🎨</div>
              <div class="text-gray-300 text-sm font-semibold">
                Modern Design
              </div>
            </div>
            <div class="glassmorphism p-6 rounded-xl">
              <div class="text-4xl mb-2">⚡</div>
              <div class="text-gray-300 text-sm font-semibold">
                Fast Performance
              </div>
            </div>
            <div class="glassmorphism p-6 rounded-xl">
              <div class="text-4xl mb-2">🔒</div>
              <div class="text-gray-300 text-sm font-semibold">
                Secure Development
              </div>
            </div>
            <div class="glassmorphism p-6 rounded-xl">
              <div class="text-4xl mb-2">💬</div>
              <div class="text-gray-300 text-sm font-semibold">
                Direct Communication
              </div>
            </div>
          </div>
        </div>

        <!-- Tier Cards -->
        <div class="mb-32">
          <h3 class="text-5xl font-bold text-center mb-4">
            Tier-Scaled Architecture
          </h3>
          <p class="text-center text-gray-400 mb-16 text-xl">
            Precision-engineered solutions for every growth stage
          </p>

          <div class="grid lg:grid-cols-3 gap-10">
            <!-- Basic -->
            <div
              class="tier-card glassmorphism p-8 rounded-3xl border-2 border-blue-500/30 hover:border-blue-500 group"
            >
              <div class="text-5xl mb-6 float-animation">📱</div>
              <h4 class="text-3xl font-bold mb-3 text-blue-400">Basic Tier</h4>
              <p class="text-gray-300 mb-6">
                Perfect for startups. Clean, focused architecture with essential
                features.
              </p>
              <div class="text-5xl font-bold mb-2">
                <span
                  class="bg-gradient-to-r from-blue-400 to-blue-600 bg-clip-text text-transparent"
                  >$400</span
                >
                <span class="text-2xl text-gray-400">+</span>
              </div>
              <p class="text-sm text-gray-400 mb-8">Starting price</p>
              <div class="space-y-3 mb-8">
                <div class="flex items-center gap-3">
                  <span class="text-blue-400">✓</span> Responsive Design
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-blue-400">✓</span> Core SEO
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-blue-400">✓</span> HTTPS Security
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-blue-400">✓</span> Contact Forms
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-blue-400">✓</span> Analytics
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-blue-400">✓</span> 1-2 Week Delivery
                </div>
              </div>
              <button
                onclick="showRequestForm()"
                class="w-full py-4 bg-gradient-to-r from-blue-600 to-blue-700 rounded-xl font-bold hover:scale-105 transition"
              >
                Select Basic
              </button>
            </div>

            <!-- Advanced -->
            <div
              class="tier-card glassmorphism p-8 rounded-3xl border-2 border-purple-500/50 hover:border-purple-500 transform scale-105 shadow-2xl"
            >
              <div
                class="absolute top-0 left-1/2 transform -translate-x-1/2 -translate-y-1/2"
              >
                <span
                  class="bg-gradient-to-r from-purple-600 to-pink-600 px-6 py-2 rounded-full text-sm font-bold"
                  >⭐ MOST POPULAR</span
                >
              </div>
              <div
                class="text-5xl mb-6 mt-6 float-animation"
                style="animation-delay: 1s"
              >
                🚀
              </div>
              <h4 class="text-3xl font-bold mb-3 text-purple-400">
                Advanced Tier
              </h4>
              <p class="text-gray-300 mb-6">
                For growing businesses. Interactive components and enhanced
                security.
              </p>
              <div class="text-5xl font-bold mb-2">
                <span
                  class="bg-gradient-to-r from-purple-400 to-pink-600 bg-clip-text text-transparent"
                  >$699</span
                >
                <span class="text-2xl text-gray-400">+</span>
              </div>
              <p class="text-sm text-gray-400 mb-8">Starting price</p>
              <div class="space-y-3 mb-8">
                <div class="flex items-center gap-3">
                  <span class="text-purple-400">✓</span> Everything in Basic +
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-purple-400">✓</span> Interactive UI
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-purple-400">✓</span> User Authentication
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-purple-400">✓</span> Payment Gateway
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-purple-400">✓</span> Enhanced Security
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-purple-400">✓</span> Advanced Analytics
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-purple-400">✓</span> 2-3 Week Delivery
                </div>
              </div>
              <button
                onclick="showRequestForm()"
                class="w-full py-4 bg-gradient-to-r from-purple-600 via-pink-600 to-purple-700 rounded-xl font-bold hover:scale-105 transition"
              >
                Select Advanced
              </button>
            </div>

            <!-- Pro -->
            <div
              class="tier-card glassmorphism p-8 rounded-3xl border-2 border-emerald-500/30 hover:border-emerald-500 group"
            >
              <div
                class="text-5xl mb-6 float-animation"
                style="animation-delay: 2s"
              >
                🏛️
              </div>
              <h4 class="text-3xl font-bold mb-3 text-emerald-400">Pro Tier</h4>
              <p class="text-gray-300 mb-6">
                Enterprise-grade. Custom architecture and real-time systems.
              </p>
              <div class="text-5xl font-bold mb-2">
                <span
                  class="bg-gradient-to-r from-emerald-400 to-teal-600 bg-clip-text text-transparent"
                  >$999</span
                >
                <span class="text-2xl text-gray-400">+</span>
              </div>
              <p class="text-sm text-gray-400 mb-8">Custom pricing</p>
              <div class="space-y-3 mb-8">
                <div class="flex items-center gap-3">
                  <span class="text-emerald-400">✓</span> Everything in Advanced
                  +
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-emerald-400">✓</span> Custom Architecture
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-emerald-400">✓</span> Real-time Processing
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-emerald-400">✓</span> Enterprise Security
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-emerald-400">✓</span> API Development
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-emerald-400">✓</span> Dedicated Support
                </div>
                <div class="flex items-center gap-3">
                  <span class="text-emerald-400">✓</span> 4-6 Week Delivery
                </div>
              </div>
              <button
                onclick="showRequestForm()"
                class="w-full py-4 bg-gradient-to-r from-emerald-600 to-teal-700 rounded-xl font-bold hover:scale-105 transition"
              >
                Select Pro
              </button>
            </div>
          </div>
        </div>

        <!-- Lead Capture -->
        <div class="max-w-3xl mx-auto">
          <div class="glassmorphism p-12 rounded-3xl border border-blue-500/30">
            <h3 class="text-4xl font-bold mb-4 text-center">
              Start Your Transformation
            </h3>
            <p class="text-gray-300 mb-8 text-center text-lg">
              Get a personalized proposal for your project needs
            </p>
            <form
              action="https://formspree.io/f/mqavjvqy"
              method="POST"
              class="space-y-6"
            >
              <div class="grid md:grid-cols-2 gap-6">
                <input
                  type="text"
                  name="name"
                  required
                  placeholder="Your Name"
                  class="w-full px-4 py-3 bg-white/5 border border-white/10 rounded-xl text-white focus:ring-2 focus:ring-blue-500 transition"
                />
                <input
                  type="email"
                  name="email"
                  required
                  placeholder="Email Address"
                  class="w-full px-4 py-3 bg-white/5 border border-white/10 rounded-xl text-white focus:ring-2 focus:ring-blue-500 transition"
                />
              </div>
              <input
                type="text"
                name="project"
                required
                placeholder="Project Vision (one sentence)"
                class="w-full px-4 py-3 bg-white/5 border border-white/10 rounded-xl text-white focus:ring-2 focus:ring-blue-500 transition"
              />
              <input
                type="hidden"
                name="_subject"
                value="New Lead from Architectura Web"
              />
              <button
                type="submit"
                class="w-full py-4 bg-gradient-to-r from-blue-600 via-purple-600 to-pink-600 text-white rounded-xl font-bold hover:scale-105 transition shadow-xl gradient-animate"
              >
                Get My Proposal →
              </button>
              <p class="text-xs text-gray-400 text-center">
                ✓ Free consultation • ✓ No commitment required
              </p>
            </form>
          </div>
        </div>
      </div>
    </div>

    <!-- PORTFOLIO VIEW -->
    <div id="portfolioView" class="hidden fade-in">
      <div class="max-w-7xl mx-auto px-6 py-20">
        <h2 class="text-6xl font-bold text-center mb-6">
          Interactive Portfolio Demos
        </h2>
        <p class="text-center text-gray-400 mb-16 text-xl">
          Click each tier to explore fully functional demonstrations showcasing
          tier-specific complexity
        </p>

        <div class="grid md:grid-cols-3 gap-10 mb-16">
          <div
            onclick="showMockup('basic')"
            class="cursor-pointer glassmorphism p-8 rounded-2xl border-2 border-blue-500/30 hover:border-blue-500 hover:transform hover:-translate-y-4 transition-all duration-300 group"
          >
            <div
              class="h-48 bg-gradient-to-r from-blue-500 to-blue-700 rounded-xl flex items-center justify-center text-3xl mb-6 group-hover:scale-105 transition-transform"
            >
              <div class="text-center text-white">
                <div class="text-5xl mb-2">📱</div>
                <div class="font-bold text-2xl">Basic Tier</div>
              </div>
            </div>
            <h3 class="text-2xl font-bold mb-3 text-blue-400">
              Garden Bistro Restaurant
            </h3>
            <p class="text-gray-300 mb-4">
              Clean, focused restaurant website with essential features and
              mobile-first design.
            </p>
            <div class="space-y-2 text-sm mb-6">
              <div class="flex items-center gap-2">
                <span class="text-blue-400">✓</span> Static Content Structure
              </div>
              <div class="flex items-center gap-2">
                <span class="text-blue-400">✓</span> Mobile-Responsive Layout
              </div>
              <div class="flex items-center gap-2">
                <span class="text-blue-400">✓</span> Basic Contact Forms
              </div>
              <div class="flex items-center gap-2">
                <span class="text-blue-400">✓</span> Essential Security (HTTPS)
              </div>
            </div>
            <button
              class="w-full py-3 bg-blue-600 hover:bg-blue-700 rounded-xl font-bold transition"
            >
              View Interactive Demo →
            </button>
          </div>

          <div
            onclick="showMockup('advanced')"
            class="cursor-pointer glassmorphism p-8 rounded-2xl border-2 border-purple-500/50 hover:border-purple-500 hover:transform hover:-translate-y-4 transition-all duration-300 group transform scale-105"
          >
            <div
              class="absolute top-0 left-1/2 transform -translate-x-1/2 -translate-y-1/2"
            >
              <span
                class="bg-gradient-to-r from-purple-600 to-pink-600 px-4 py-1 rounded-full text-xs font-bold"
                >⭐ MOST POPULAR</span
              >
            </div>
            <div
              class="h-48 bg-gradient-to-r from-purple-600 to-purple-800 rounded-xl flex items-center justify-center text-3xl mb-6 mt-4 group-hover:scale-105 transition-transform"
            >
              <div class="text-center text-white">
                <div class="text-5xl mb-2">🚀</div>
                <div class="font-bold text-2xl">Advanced Tier</div>
              </div>
            </div>
            <h3 class="text-2xl font-bold mb-3 text-purple-400">
              Peak Blend Coffee Shop
            </h3>
            <p class="text-gray-300 mb-4">
              Full e-commerce platform with subscriptions, user accounts, and
              interactive features.
            </p>
            <div class="space-y-2 text-sm mb-6">
              <div class="flex items-center gap-2">
                <span class="text-purple-400">✓</span> Dynamic Content & Filters
              </div>
              <div class="flex items-center gap-2">
                <span class="text-purple-400">✓</span> User Authentication
                System
              </div>
              <div class="flex items-center gap-2">
                <span class="text-purple-400">✓</span> Shopping Cart & Checkout
              </div>
              <div class="flex items-center gap-2">
                <span class="text-purple-400">✓</span> Enhanced Security Suite
              </div>
            </div>
            <button
              class="w-full py-3 bg-gradient-to-r from-purple-600 to-pink-600 hover:from-purple-700 hover:to-pink-700 rounded-xl font-bold transition"
            >
              View Interactive Demo →
            </button>
          </div>

          <div
            onclick="showMockup('pro')"
            class="cursor-pointer glassmorphism p-8 rounded-2xl border-2 border-emerald-500/30 hover:border-emerald-500 hover:transform hover:-translate-y-4 transition-all duration-300 group"
          >
            <div
              class="h-48 bg-gradient-to-r from-emerald-600 to-emerald-800 rounded-xl flex items-center justify-center text-3xl mb-6 group-hover:scale-105 transition-transform"
            >
              <div class="text-center text-white">
                <div class="text-5xl mb-2">🏛️</div>
                <div class="font-bold text-2xl">Pro Tier</div>
              </div>
            </div>
            <h3 class="text-2xl font-bold mb-3 text-emerald-400">
              CloudSync Enterprise Platform
            </h3>
            <p class="text-gray-300 mb-4">
              Enterprise file management with real-time collaboration and
              advanced integrations.
            </p>
            <div class="space-y-2 text-sm mb-6">
              <div class="flex items-center gap-2">
                <span class="text-emerald-400">✓</span> Real-time Data Sync
              </div>
              <div class="flex items-center gap-2">
                <span class="text-emerald-400">✓</span> Complex User Permissions
              </div>
              <div class="flex items-center gap-2">
                <span class="text-emerald-400">✓</span> Live Activity Feeds
              </div>
              <div class="flex items-center gap-2">
                <span class="text-emerald-400">✓</span> Enterprise Security
                Features
              </div>
            </div>
            <button
              class="w-full py-3 bg-gradient-to-r from-emerald-600 to-teal-700 hover:from-emerald-700 hover:to-teal-800 rounded-xl font-bold transition"
            >
              View Interactive Demo →
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- MOCKUP VIEWER -->
    <div
      id="mockupViewer"
      class="hidden fixed inset-0 bg-black/80 backdrop-blur-sm z-50 overflow-y-auto"
    >
      <div class="min-h-screen p-6">
        <div class="max-w-7xl mx-auto">
          <div class="flex justify-between items-center mb-6">
            <h3 id="mockupTitle" class="text-3xl font-bold"></h3>
            <button
              onclick="closeMockup()"
              class="text-4xl hover:text-gray-300 transition"
            >
              ×
            </button>
          </div>
          <div
            id="mockupContent"
            class="bg-white rounded-2xl shadow-2xl overflow-hidden"
          ></div>
        </div>
      </div>
    </div>

    <!-- PRICING VIEW -->
    <div id="pricingView" class="hidden fade-in">
      <div class="max-w-7xl mx-auto px-6 py-20">
        <h2 class="text-6xl font-bold text-center mb-6">Transparent Pricing</h2>
        <p class="text-center text-gray-400 mb-16 text-xl">
          Starting prices from $400 to $999 - Custom quotes available
        </p>

        <div class="max-w-4xl mx-auto glassmorphism p-12 rounded-3xl">
          <div class="space-y-8">
            <div
              class="flex justify-between items-center border-b border-white/10 pb-6"
            >
              <div>
                <h3 class="text-2xl font-bold text-blue-400">Basic Tier</h3>
                <p class="text-gray-400">
                  1-5 page website • 1-2 week timeline
                </p>
              </div>
              <div class="text-4xl font-bold">$400+</div>
            </div>
            <div
              class="flex justify-between items-center border-b border-white/10 pb-6"
            >
              <div>
                <h3 class="text-2xl font-bold text-purple-400">
                  Advanced Tier
                </h3>
                <p class="text-gray-400">
                  Full-featured platform • 2-3 week timeline
                </p>
              </div>
              <div class="text-4xl font-bold">$699+</div>
            </div>
            <div class="flex justify-between items-center">
              <div>
                <h3 class="text-2xl font-bold text-emerald-400">Pro Tier</h3>
                <p class="text-gray-400">
                  Enterprise solution • 4-6 week timeline
                </p>
              </div>
              <div class="text-4xl font-bold">$999+</div>
            </div>
          </div
