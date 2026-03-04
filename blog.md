---
layout: default
title: Blog Archive
permalink: /blog/
---

<section class="py-32 px-6 max-w-5xl mx-auto">
    <h1 class="text-4xl font-extrabold mb-12 tracking-tight">System Logs <span class="text-zinc-500">/ Blog</span></h1>

    <div class="space-y-8">
        {% for post in site.posts %}
        <div class="glass-card p-6 rounded-2xl flex justify-between items-center">
            <div>
                <span class="text-xs font-mono text-indigo-500 block mb-2">{{ post.date | date: "%Y-%m-%d" }}</span>
                <a href="{{ post.url }}" class="text-xl font-bold hover:text-indigo-400 transition-colors">
                    {{ post.title }}
                </a>
                <p class="text-zinc-400 text-sm mt-2">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
            </div>
            <div class="text-zinc-600 font-mono text-xs hidden md:block">
                [ACCESS_GRANTED]
            </div>
        </div>
        {% else %}
        <p class="text-zinc-500 italic">Logs are empty. Waiting for data input...</p>
        {% endfor %}
    </div>
</section>
