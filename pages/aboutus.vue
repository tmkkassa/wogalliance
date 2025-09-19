<template>
    <div>
        <Navbar :navlight="true" />

        <!-- Hero Section -->
        <section class="relative table w-full py-32 lg:py-44 bg-no-repeat bg-center bg-cover"
            :style="{ backgroundImage: `url(${bg})` }">
            <div class="absolute inset-0 bg-black opacity-80"></div>
            <div class="container relative">
                <div class="grid grid-cols-1 text-center mt-10">
                    <h3 class="md:text-4xl text-3xl md:leading-normal leading-normal font-bold text-white mb-4">About
                        WoGA</h3>
                    <p class="text-lg text-gray-200 max-w-3xl mx-auto">Wolayta Global Alliance - Building bridges
                        between communities, fostering unity, and promoting human rights worldwide.</p>
                </div>
            </div>
        </section>

        <div class="relative">
            <div class="shape overflow-hidden z-1 text-white dark:text-slate-900">
                <svg viewBox="0 0 2880 48" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M0 48H1437.5H2880V0H2160C1442.5 52 720 0 720 0H0V48Z" fill="currentColor"></path>
                </svg>
            </div>
        </div>

        <!-- Who We Are Section -->
        <section class="relative lg:py-24 py-16 bg-gray-50 dark:bg-slate-900">
            <div class="container relative">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <div class="lg:order-2">
                        <div class="relative">
                            <div class="relative z-10">
                                <img :src="bg" class="rounded-lg shadow-2xl" alt="Community Unity">
                            </div>
                            <div
                                class="absolute -bottom-6 -left-6 w-24 h-24 bg-gradient-to-r from-primary to-blue-400 rounded-full opacity-20">
                            </div>
                            <div
                                class="absolute -top-6 -right-6 w-32 h-32 bg-gradient-to-r from-blue-400 to-primary rounded-full opacity-20">
                            </div>
                        </div>
                    </div>

                    <div class="lg:order-1">
                        <div class="flex items-center mb-6">
                            <div
                                class="w-12 h-12 bg-gradient-to-r from-primary to-blue-400 rounded-lg flex items-center justify-center mr-4 shadow-lg">
                                <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                        d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z">
                                    </path>
                                </svg>
                            </div>
                            <h2 class="text-3xl font-bold text-gray-900 dark:text-white">Who We Are</h2>
                        </div>
                        <p class="text-lg text-gray-600 dark:text-gray-300 leading-relaxed mb-6">
                            We are voluntarily associated individuals passionate about supporting smooth integration and
                            social cohesion of immigrants and contributing to the humanitarian action, human rights and
                            social development of the community of origin.
                        </p>
                        <p class="text-lg text-gray-600 dark:text-gray-300 leading-relaxed">
                            Also, we value bridging the emotional and social connection of the Wolayata community
                            members living in the United States and beyond.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Vision & Mission Section -->
        <section class="relative lg:py-24 py-16">
            <div class="container relative">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                    <!-- Vision Card -->
                    <div
                        class="group p-8 rounded-2xl bg-gradient-to-br from-blue-50 to-blue-100 dark:from-slate-800 dark:to-slate-700 border border-blue-200 dark:border-slate-600 hover:shadow-xl transition-all duration-300">
                        <div
                            class="w-16 h-16 bg-gradient-to-r from-primary to-blue-400 rounded-xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300 shadow-lg">
                            <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-4">Our Vision</h3>
                        <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
                            We envision a world where human rights are respected, democratic culture is promoted, people
                            achieve inclusive and equitable opportunity to develop to their full potential in a
                            community, and an environment that responds effectively to the needs of their members is
                            realized.
                        </p>
                    </div>

                    <!-- Mission Card -->
                    <div
                        class="group p-8 rounded-2xl bg-gradient-to-br from-blue-100 to-blue-50 dark:from-slate-800 dark:to-slate-700 border border-blue-200 dark:border-slate-600 hover:shadow-xl transition-all duration-300">
                        <div
                            class="w-16 h-16 bg-gradient-to-r from-blue-400 to-primary rounded-xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300 shadow-lg">
                            <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                            </svg>
                        </div>
                        <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-4">Our Mission</h3>
                        <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
                            To achieve our vision, we implement a mission of organizing vibrant and functionally strong
                            community structures providing targeted community service to the Wolayta diaspora and
                            engaging in sociocultural, civic and humanitarian affairs affecting the community of origin
                            back home.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!--Objectives Section -->
        <section class="relative lg:py-24 py-16 bg-gray-50 dark:bg-slate-900">
            <div class="container relative">
                <div class="text-center mb-16">
                    <h2 class="text-4xl font-bold text-gray-900 dark:text-white mb-6">Objectives</h2>
                    <p class="text-xl text-gray-600 dark:text-gray-300 max-w-4xl mx-auto">
                        WoGA is registered as a non-profit, non-governmental alliance of individuals committed to
                        fostering solidarity, mutual assistance, and strong social bonds among our community members.
                    </p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Service Card 1 -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-primary to-blue-400 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Community Networking</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            Form cohesive neighborhood and metro-level networking to respond to immediate social needs
                            informed by specialized bylaws.
                        </p>
                    </div>

                    <!-- Service Card 2 -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-blue-400 to-primary rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Cultural Preservation</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            Preserve and promote Wolayta cultural values while building a vibrant diaspora community
                            that effectively links to the community of origin.
                        </p>
                    </div>

                    <!-- Service Card 3 -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-primary to-blue-400 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197m13.5-9a2.5 2.5 0 11-5 0 2.5 2.5 0 015 0z">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Humanitarian Support</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            Engage in sociocultural, civic and humanitarian affairs affecting the community of origin in
                            Ethiopia.
                        </p>
                    </div>

                    <!-- Service Card 4 -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-blue-400 to-primary rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Global Outreach</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            Network to intensify experience and impact among the Wolayta diaspora on a global scale.
                        </p>
                    </div>

                    <!-- Service Card 5 -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-primary to-blue-400 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Family Support</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            Support families in times of social need and provide mutual assistance to strengthen
                            community bonds.
                        </p>
                    </div>

                    <!-- Service Card 6 -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-blue-400 to-primary rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019 9">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Integration Support</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            Support smooth integration and social cohesion of immigrants in their new communities.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- What We Do Section -->
        <section class="relative lg:py-24 py-16">
            <div class="container relative">
                <div class="text-center mb-16">
                    <h2 class="text-4xl font-bold text-gray-900 dark:text-white mb-6">What We Do</h2>
                    <p class="text-xl text-gray-600 dark:text-gray-300 max-w-4xl mx-auto">
                        Our comprehensive approach to addressing community needs and promoting social justice through
                        various initiatives and programs.
                    </p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- What We Do Card 1 -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-primary to-blue-400 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Policy Recommendation</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            We develop and advocate for evidence-based policy recommendations that address community
                            needs and promote social justice.
                        </p>
                    </div>

                    <!-- What We Do Card 2 -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-blue-400 to-primary rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-2.5L13.732 4c-.77-.833-1.964-.833-2.732 0L3.732 16.5c-.77.833.192 2.5 1.732 2.5z">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Emerging Injustice</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            We identify, document, and respond to emerging injustices within our communities and
                            advocate for systemic change.
                        </p>
                    </div>

                    <!-- What We Do Card 3 -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-primary to-blue-400 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M9 5H7a2 2 0 00-2 2v10a2 2 0 002 2h8a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-3 7h3m-3 4h3m-6-4h.01M9 16h.01">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Research Findings and
                            Further Directions</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            We conduct research to understand community challenges and develop evidence-based solutions
                            for sustainable impact.
                        </p>
                    </div>

                    <!-- What We Do Card 4 -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-blue-400 to-primary rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Ongoing Projects</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            We implement and manage various ongoing projects that directly benefit our community members
                            and address their needs.
                        </p>
                    </div>

                    <!-- What We Do Card 5 -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-primary to-blue-400 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Incident of Humanitarian
                            Crisis</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            We respond to humanitarian crises by providing immediate assistance and long-term support to
                            affected community members.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Call to Action Section -->
        <section class="relative lg:py-24 py-16">
            <div class="container relative">
                <div
                    class="bg-gradient-to-r from-primary to-blue-600 rounded-3xl p-12 text-center text-white shadow-2xl">
                    <div class="max-w-4xl mx-auto">
                        <h2 class="text-4xl font-bold mb-6">Join Our Mission</h2>
                        <p class="text-xl text-blue-100 mb-8 leading-relaxed">
                            Learn more about how you can be part of our mission to build bridges between communities,
                            foster unity, and promote human rights worldwide.
                        </p>
                        <div class="flex flex-col sm:flex-row gap-4 justify-center">
                            <a href="/contactus"
                                class="inline-flex items-center px-8 py-4 bg-white text-primary font-semibold rounded-lg hover:bg-gray-100 transition-colors duration-300 shadow-lg">
                                <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                        d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z">
                                    </path>
                                </svg>
                                Get In Touch
                            </a>
                            <a href="/contactus"
                                class="inline-flex items-center px-8 py-4 bg-transparent border-2 border-white text-white font-semibold rounded-lg hover:bg-white hover:text-primary transition-all duration-300 shadow-lg">
                                <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                        d="M18 9v3m0 0v3m0-3h3m-3 0h-3m-2-5a4 4 0 11-8 0 4 4 0 018 0zM3 20a6 6 0 0112 0v1H3v-1z">
                                    </path>
                                </svg>
                                Join Our Community
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Five Year Target Section -->
        <!-- <section class="relative lg:py-24 py-16">
            <div class="container relative">
                <div class="grid grid-cols-1 text-center">
                    <h3 class="mb-6 md:text-3xl text-2xl md:leading-normal leading-normal font-semibold">Five Year
                        Target</h3>
                    <p class="text-slate-400 max-w-xl mx-auto mb-12">Our ambitious goals for the next five years to
                        expand our impact and reach</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                    <div
                        class="text-center p-6 bg-white dark:bg-slate-800 rounded-xl shadow-lg hover:shadow-xl transition-all duration-300">
                        <div class="text-4xl font-bold text-primary mb-2">500+</div>
                        <div class="text-gray-600 dark:text-gray-300">Community Members</div>
                    </div>
                    <div
                        class="text-center p-6 bg-white dark:bg-slate-800 rounded-xl shadow-lg hover:shadow-xl transition-all duration-300">
                        <div class="text-4xl font-bold text-blue-400 mb-2">5+</div>
                        <div class="text-gray-600 dark:text-gray-300">Countries</div>
                    </div>
                    <div
                        class="text-center p-6 bg-white dark:bg-slate-800 rounded-xl shadow-lg hover:shadow-xl transition-all duration-300">
                        <div class="text-4xl font-bold text-primary mb-2">10+</div>
                        <div class="text-gray-600 dark:text-gray-300">Cultural Events</div>
                    </div>
                    <div
                        class="text-center p-6 bg-white dark:bg-slate-800 rounded-xl shadow-lg hover:shadow-xl transition-all duration-300">
                        <div class="text-4xl font-bold text-blue-400 mb-2">25+</div>
                        <div class="text-gray-600 dark:text-gray-300">Humanitarian Support</div>
                    </div>
                </div>
            </div>
        </section> -->

        <div class="grid grid-cols-1 text-center">
            <h3 class="mb-6 md:text-3xl text-2xl md:leading-normal leading-normal font-semibold">Five Year
                Target</h3>
            <p class="text-slate-400 max-w-xl mx-auto mb-12">Our ambitious goals for the next five years to
                expand our impact and reach</p>
        </div>
        <!-- Stats Section -->
        <section class="relative lg:py-24 py-16 bg-gray-50 dark:bg-slate-900">
            <div class="container relative">
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                    <div class="text-center">
                        <div class="text-4xl font-bold text-primary mb-2">500+</div>
                        <div class="text-gray-600 dark:text-gray-300">Community Members</div>
                    </div>
                    <div class="text-center">
                        <div class="text-4xl font-bold text-blue-400 mb-2">5+</div>
                        <div class="text-gray-600 dark:text-gray-300">Countries</div>
                    </div>
                    <div class="text-center">
                        <div class="text-4xl font-bold text-primary mb-2">10+</div>
                        <div class="text-gray-600 dark:text-gray-300">Cultural Events</div>
                    </div>
                    <div class="text-center">
                        <div class="text-4xl font-bold text-blue-400 mb-2">25+</div>
                        <div class="text-gray-600 dark:text-gray-300">Humanitarian Support</div>
                    </div>
                </div>
            </div>
        </section>

        <Footer />
        <Switcher />
        <ScrollToTop />
    </div>
</template>

<script setup>
import bg from '@/assets/images/gallery/view2.jpeg'
</script>
