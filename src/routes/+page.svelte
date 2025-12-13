<script lang="ts">
	// Icons
	import { ArrowRight, Plus, ChevronDown, Play } from 'lucide-svelte';

	// State for FAQ
	let openFaq: number | null = null;
	const toggleFaq = (index: number) => {
		openFaq = openFaq === index ? null : index;
	};

	const faqs = [
		{ q: "What is CORELAX?", a: "CORELAX is Japan's first 24/7 unmanned recovery facility offering medical-grade AI massage chairs and oxygen capsules. Access anytime without appointments through our app-based QR entry system." },
		{ q: "How does the unmanned system work?", a: "Simply use our app to check real-time availability, enter with your QR code, and enjoy unlimited access to all equipment. Our AI monitoring ensures safety and security 24/7, with daily staff cleaning visits." },
		{ q: "What equipment is available?", a: "All our equipment is medical-grade certified: AI-powered massage chairs with customizable programs, oxygen capsules for recovery therapy, and vibration machines. Everything is included in your monthly membership." },
		{ q: "Is it safe without staff present?", a: "Yes. We use QR code entry (members only), AI-equipped surveillance cameras, and real-time monitoring by headquarters. The facility is designed to be safer than traditional spas with professional security protocols." },
		{ q: "How much does membership cost?", a: "Our standard membership is ¥1,960/month (tax included) with unlimited access. We offer special pre-registration discounts and promotional campaigns. Check our app for current offers." },
		{ q: "Where are you located?", a: "Our first location is at Mukogaoka-Yuen Station (30 seconds walk) in Kawasaki. We're actively expanding across Tokyo and major metropolitan areas. Property owners can contact us for partnership opportunities." }
	];

    // CORELAX images
    const heroImage = "/generated/image-modern-minimalist-wellness-facility-inte-1765616904497-0.webp"; 
    const massageChairImage = "/generated/image-urban-japanese-professional-in-business--1765616907940-1.webp";
    const oxygenCapsuleImage = "/generated/image-sleek-oxygen-capsule-pod-in-a-clean-mode-1765616910624-2.webp";
    const stressedCommuterImage = "/generated/image-tired-businessman-in-suit-walking-on-tok-1765616912876-3.webp";
    const facilityExteriorImage = "/generated/image-modern-unmanned-facility-exterior-at-nig-1765616916062-4.webp";
    const appImage = "/generated/image-close-up-of-person-using-smartphone-app--1765616918719-5.webp";
    const securityImage = "/generated/image-high-tech-security-camera-with-ai-monito-1765616921219-6.webp";
    const relaxingWomanImage = "/generated/image-young-japanese-professional-woman-in-cas-1765616923577-7.webp";

</script>

<!-- Header -->
<header class="fixed top-0 left-0 right-0 z-50 flex items-center justify-between px-6 py-4 bg-white/90 backdrop-blur-sm border-b border-gray-100">
	<div class="w-12">
		<a href="#membership" class="text-xs font-medium text-gray-600 hover:text-dark transition-colors">Join</a>
	</div>
	<div class="text-lg font-bold tracking-wider">CORELAX</div>
	<div class="w-12 flex justify-end">
		<button class="text-xs font-medium border border-gray-300 rounded-full px-3 py-1 hover:bg-gray-100">JP</button>
	</div>
</header>

<main class="pt-24 pb-20">
	<!-- Hero Section -->
	<section class="container-custom mb-32">
		<div class="flex flex-col items-center text-center mb-12">
			<p class="text-xs text-gray-500 mb-4 max-w-xs">Medical-grade recovery<br>available 24/7, no appointments needed</p>
			<h1 class="text-6xl md:text-8xl font-medium tracking-tight mb-8">Recover on<br>your schedule</h1>
		</div>

		<div class="relative w-full aspect-[16/9] md:aspect-[21/9] rounded-3xl overflow-hidden mb-12 bg-gray-200">
			<img src={heroImage} alt="CORELAX modern wellness facility interior" class="w-full h-full object-cover" />
		</div>

		<div class="max-w-3xl mx-auto text-center">
			<p class="text-xl md:text-2xl leading-relaxed font-light text-gray-800">
				Japan's first 24/7 unmanned recovery facility. Access medical-grade AI massage chairs and oxygen capsules anytime, without the premium spa price tag.
			</p>
		</div>
	</section>

	<!-- Story / Video Section -->
	<section class="container-custom mb-40">
		<div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
			<div class="max-w-sm">
				<p class="text-sm leading-relaxed text-gray-600">
					Urban professionals deserve daily recovery without the hassle of appointments or premium prices. See how we're building the future of wellness infrastructure across Japan.
				</p>
			</div>
			<div class="relative aspect-video rounded-xl overflow-hidden bg-gray-800 group cursor-pointer">
				<img src={stressedCommuterImage} alt="Urban commuter lifestyle" class="w-full h-full object-cover opacity-80 group-hover:opacity-60 transition-opacity" />
				<div class="absolute inset-0 flex items-center justify-center">
					<div class="w-12 h-12 rounded-full bg-white/20 backdrop-blur-md flex items-center justify-center text-white">
						<Play size={20} fill="currentColor" />
					</div>
				</div>
				<div class="absolute bottom-4 left-4 text-white text-sm font-medium">01. The daily stress problem</div>
			</div>
		</div>
	</section>

	<!-- Typography Section -->
	<section class="container-custom mb-40">
		<div class="flex flex-col text-7xl md:text-9xl font-medium tracking-tighter leading-none mb-24">
			<span class="self-start">Recovery</span>
			<span class="self-center my-4 md:my-8">without</span>
			<span class="self-end">limits</span>
		</div>

		<div class="max-w-2xl mx-auto text-center">
			<p class="text-lg text-gray-600 leading-relaxed">
				No appointments. No time limits. No guilt. Just unlimited access to medical-grade recovery equipment whenever you need it. Our unmanned operations keep costs low while maintaining the highest quality standards.
			</p>
		</div>
	</section>

	<!-- Feature 1: AI Massage Chairs -->
	<section class="container-custom mb-24">
		<div class="relative w-full aspect-[16/9] rounded-3xl overflow-hidden mb-4 group">
			<img src={massageChairImage} alt="AI massage chair" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center">
				<h2 class="text-4xl md:text-6xl text-white font-medium text-center px-4 drop-shadow-lg">Medical-grade<br>AI massage chairs</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/80 text-xs">Certified therapeutic equipment</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-2 gap-4">
			<div class="bg-gray-100 rounded-3xl p-8 flex items-end">
				<p class="text-sm text-gray-600 leading-relaxed max-w-xs">
					Every massage chair is medical-grade certified with AI-powered customization. Choose from deep tissue, relaxation, or recovery programs. Use them as long as you want, as often as you want—all included in your membership.
				</p>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden">
				<img src={relaxingWomanImage} alt="Relaxing in massage chair" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">01. Unlimited sessions, no time limits</div>
			</div>
		</div>
	</section>

	<!-- Feature 2: 24/7 Access -->
	<section class="container-custom mb-24">
		<div class="relative w-full aspect-[16/9] rounded-3xl overflow-hidden mb-4 group">
			<img src={facilityExteriorImage} alt="CORELAX facility exterior" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center">
				<h2 class="text-4xl md:text-6xl text-white font-medium text-center px-4 drop-shadow-lg">Open 24/7<br>No appointments</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/80 text-xs">Access anytime, even at 3 AM</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
			<div class="bg-gray-100 rounded-3xl p-8 flex items-end md:col-span-1">
				<p class="text-sm text-gray-600 leading-relaxed">
					Traditional spas require appointments weeks in advance. CORELAX is always open. Check real-time availability on our app, walk in with your QR code, and start recovering immediately. Perfect for busy commuters.
				</p>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src={appImage} alt="CORELAX app" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">01. Real-time crowding status</div>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src={securityImage} alt="Security system" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">02. AI-monitored security</div>
			</div>
		</div>
	</section>

	<!-- Feature 3: Oxygen Capsules -->
	<section class="container-custom mb-32">
		<div class="relative w-full aspect-[16/9] rounded-3xl overflow-hidden mb-4 group">
			<img src={oxygenCapsuleImage} alt="Oxygen capsule" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center">
				<h2 class="text-4xl md:text-6xl text-white font-medium text-center px-4 drop-shadow-lg">Premium oxygen<br>therapy</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/80 text-xs">Advanced recovery technology</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
			<div class="bg-gray-100 rounded-3xl p-8 flex items-end md:col-span-1">
				<p class="text-sm text-gray-600 leading-relaxed">
					Our oxygen capsules provide concentrated oxygen therapy for deep recovery. Popular with athletes and busy professionals, they help reduce fatigue, improve sleep quality, and accelerate physical recovery. Available as an optional add-on to your membership.
				</p>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src={massageChairImage} alt="Recovery equipment" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">01. Combine with massage therapy</div>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src={relaxingWomanImage} alt="Deep relaxation" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">02. Complete recovery experience</div>
			</div>
		</div>
	</section>

	<!-- Technology Section -->
	<section class="bg-gray-50 py-32">
		<div class="container-custom">
			<div class="flex flex-col items-center text-center mb-16">
				<h2 class="text-5xl md:text-7xl font-medium tracking-tight text-dark mb-12">Unmanned,<br>but never unattended</h2>
				
				<div class="relative w-full max-w-4xl aspect-square md:aspect-[16/9] mb-12">
					<img src={securityImage} alt="AI security monitoring" class="w-full h-full object-cover rounded-2xl" />
				</div>

				<div class="max-w-2xl mx-auto mb-12">
					<p class="text-xl text-gray-700 leading-relaxed">
						Our AI-powered monitoring system ensures safety and security 24/7. QR code entry keeps non-members out, while real-time surveillance protects members inside. Daily staff visits maintain pristine cleanliness standards.
					</p>
				</div>

				<div class="relative w-full max-w-3xl aspect-video rounded-2xl overflow-hidden mb-12 bg-gray-800">
					<img src={appImage} alt="CORELAX app interface" class="w-full h-full object-cover opacity-80" />
					<div class="absolute inset-0 flex items-center justify-center">
						<div class="w-16 h-16 rounded-full bg-white/20 backdrop-blur-md flex items-center justify-center text-white">
							<Play size={24} fill="currentColor" />
						</div>
					</div>
					<div class="absolute bottom-4 left-4 text-white text-xs font-medium">01. How the app works</div>
				</div>

				<div class="text-center max-w-md mx-auto text-sm text-gray-600 mb-8">
					Lower operating costs mean lower membership fees. We pass the savings from unmanned operations directly to you, making medical-grade recovery accessible to everyone.
				</div>

				<div class="flex gap-8 justify-center text-sm font-medium">
					<a href="#membership" class="border-b border-gray-400 pb-0.5 hover:border-black transition-colors">Join Now</a>
					<a href="#locations" class="border-b border-gray-400 pb-0.5 hover:border-black transition-colors">Find a Location</a>
				</div>
			</div>
		</div>
	</section>

	<!-- Membership Section -->
	<section class="py-32 bg-white" id="membership">
		<div class="container-custom">
			<div class="text-center mb-16">
				<h2 class="text-5xl md:text-7xl font-medium tracking-tight mb-12">Simple pricing,<br>unlimited access</h2>
				
				<div class="inline-flex bg-gray-100 rounded-full p-1 shadow-sm border border-gray-200">
					<button class="px-6 py-2 rounded-full bg-white text-sm font-medium shadow-sm">Monthly</button>
					<button class="px-6 py-2 rounded-full text-gray-500 hover:bg-gray-50 text-sm font-medium">Annual</button>
				</div>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
				<!-- Card 1 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden group">
					<img src={massageChairImage} alt="Massage chairs" class="w-full h-full object-cover" />
					<div class="absolute inset-0 bg-black/40 p-8 flex flex-col justify-between opacity-0 group-hover:opacity-100 transition-opacity duration-300">
						<div class="text-white">
							<h3 class="font-bold mb-2">Medical-grade equipment</h3>
							<p class="text-xs leading-relaxed opacity-90">All massage chairs and equipment are certified medical devices. We maintain the highest quality standards with daily professional cleaning.</p>
						</div>
					</div>
				</div>

				<!-- Card 2 - Pricing -->
				<div class="bg-dark text-white rounded-3xl p-8 flex flex-col justify-center">
					<div class="text-5xl font-bold mb-2">¥1,960</div>
					<p class="text-sm opacity-80 mb-6">per month (tax included)</p>
					<h3 class="font-medium text-lg mb-4">Standard Membership</h3>
					<ul class="text-sm space-y-2 opacity-90">
						<li>✓ Unlimited massage chair access</li>
						<li>✓ Vibration machines included</li>
						<li>✓ 24/7 facility access</li>
						<li>✓ No time limits</li>
						<li>✓ Real-time app monitoring</li>
					</ul>
				</div>

				<!-- Card 3 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden bg-gray-100">
					<img src={oxygenCapsuleImage} alt="Oxygen capsule" class="w-full h-full object-cover" />
                    <div class="absolute bottom-8 left-8 text-dark max-w-[200px]">
                        <h3 class="font-bold text-sm mb-1">Oxygen Capsule Add-on</h3>
                        <p class="text-xs opacity-80">Premium recovery therapy available as optional upgrade</p>
                    </div>
				</div>

                <!-- Card 4 -->
				<div class="bg-gray-100 rounded-3xl p-8 flex flex-col justify-center">
					<h3 class="font-medium text-lg mb-4">No appointments needed</h3>
					<p class="text-sm text-gray-600 leading-relaxed">
						Check real-time availability on our app and walk right in. Perfect for spontaneous recovery sessions after work or late-night stress relief.
					</p>
				</div>

                <!-- Card 5 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden">
					<img src={facilityExteriorImage} alt="Facility exterior" class="w-full h-full object-cover" />
                    <div class="absolute top-8 left-8 text-white max-w-[200px]">
                        <h3 class="font-bold text-sm mb-1">Prime locations</h3>
                        <p class="text-xs opacity-90 drop-shadow">30 seconds from Mukogaoka-Yuen Station. More locations opening soon.</p>
                    </div>
				</div>

                 <!-- Card 6 -->
				<div class="bg-gray-100 rounded-3xl p-8 flex flex-col justify-center">
					<h3 class="font-medium text-lg mb-4">Pre-registration discount</h3>
					<p class="text-sm text-gray-600 leading-relaxed mb-4">
						Lifetime 10% discount for early members. Lock in ¥1,782/month forever with our pre-registration plan.
					</p>
					<a href="#" class="text-sm font-medium border-b border-dark pb-0.5 hover:opacity-60 transition-opacity inline-block">Learn more</a>
				</div>
			</div>
            
            <div class="flex justify-center mt-12">
                 <button class="bg-dark text-white px-8 py-4 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">
					Start your membership
				</button>
            </div>
		</div>
	</section>

	<!-- Expansion Section -->
	<section class="bg-gray-50 py-32" id="locations">
		<div class="container-custom flex flex-col items-center text-center">
			<h2 class="text-5xl md:text-7xl font-medium tracking-tight mb-8">Expanding across<br>Japan</h2>
			
			<p class="text-lg text-gray-600 max-w-2xl mb-12">
				We're building the future of wellness infrastructure. Scaling to 100 locations across Tokyo and major metropolitan areas.
			</p>
			
			<div class="grid grid-cols-1 md:grid-cols-2 gap-8 w-full max-w-4xl mb-12">
				<div class="bg-white rounded-2xl p-8 text-left">
					<h3 class="font-bold text-xl mb-4">Current Location</h3>
					<p class="text-sm text-gray-600 mb-2">CORELAX Mukogaoka-Yuen</p>
					<p class="text-xs text-gray-500 leading-relaxed">
						Kanagawa Prefecture, Kawasaki City<br>
						30 seconds from Mukogaoka-Yuen Station<br>
						Odakyu Line
					</p>
				</div>
				
				<div class="bg-dark text-white rounded-2xl p-8 text-left">
					<h3 class="font-bold text-xl mb-4">Property Owners</h3>
					<p class="text-sm opacity-90 mb-4">
						Have a vacant property? Partner with us and receive 2 months' rent as referral fee.
					</p>
					<a href="#" class="text-sm font-medium border-b border-white/30 pb-0.5 hover:border-white transition-colors inline-block">
						Learn more about partnerships
					</a>
				</div>
			</div>
			
			<button class="bg-dark text-white px-8 py-3 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">
				View all locations
			</button>
		</div>
	</section>

	<!-- FAQ Section -->
	<section class="py-32 container-custom">
		<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
			<div>
				<h2 class="text-sm font-medium text-gray-500 uppercase tracking-wide">Frequently asked questions</h2>
			</div>
			<div class="md:col-span-2">
				<div class="space-y-4">
					{#each faqs as faq, i}
						<div class="border-b border-gray-200 pb-4">
							<button 
								class="w-full flex items-center justify-between text-left py-4 focus:outline-none group"
								onclick={() => toggleFaq(i)}
							>
								<span class="text-lg font-medium group-hover:text-gray-600 transition-colors">{faq.q}</span>
								<ChevronDown class="transition-transform duration-300 {openFaq === i ? 'rotate-180' : ''}" />
							</button>
							{#if openFaq === i}
								<div class="pb-4 text-gray-600 leading-relaxed">
									{faq.a}
								</div>
							{/if}
						</div>
					{/each}
				</div>
			</div>
		</div>
	</section>
</main>

<!-- Footer -->
<footer class="bg-gray-100 pt-20 pb-8 rounded-t-[3rem] mt-[-2rem] relative z-10">
	<div class="container-custom">
		<!-- Black CTA Box -->
		<div class="bg-dark text-white rounded-3xl p-12 md:p-24 text-center mb-20 relative overflow-hidden">
			<div class="relative z-10">
				<h2 class="text-2xl md:text-4xl font-medium mb-8">Ready to recover on your schedule? <span class="text-gray-400">Join thousands of urban professionals finding daily relief.</span></h2>
				<a href="#membership" class="inline-flex items-center border border-white/30 rounded-full px-6 py-2 hover:bg-white/10 transition-colors text-sm">
					Start your membership <ArrowRight size={16} class="ml-2" />
				</a>
			</div>
		</div>

		<!-- Footer Links -->
		<div class="grid grid-cols-2 md:grid-cols-4 gap-8 mb-20 text-sm">
			<div class="col-span-2 md:col-span-1">
				<p class="mb-4 font-medium">Get updates</p>
				<form class="flex border-b border-gray-400 pb-2">
					<input type="email" placeholder="Email address" class="bg-transparent border-none outline-none w-full placeholder-gray-500" />
					<button type="submit" class="font-medium">Subscribe</button>
				</form>
			</div>
			
			<div class="md:col-start-3">
				<ul class="space-y-2 text-gray-600">
					<li><a href="#membership" class="hover:text-dark transition-colors">Membership</a></li>
					<li><a href="#locations" class="hover:text-dark transition-colors">Locations</a></li>
					<li><a href="#" class="hover:text-dark transition-colors">Equipment</a></li>
				</ul>
			</div>

			<div>
				<ul class="space-y-2 text-gray-600">
					<li><a href="#" class="hover:text-dark transition-colors">About</a></li>
					<li><a href="#" class="hover:text-dark transition-colors">Property Owners</a></li>
					<li><a href="#" class="hover:text-dark transition-colors">Careers</a></li>
					<li><a href="#" class="hover:text-dark transition-colors">Press</a></li>
				</ul>
			</div>

			<div>
				<ul class="space-y-2 text-gray-600">
					<li><a href="#" class="hover:text-dark transition-colors">Instagram</a></li>
					<li><a href="#" class="hover:text-dark transition-colors">X (Twitter)</a></li>
					<li><a href="#" class="hover:text-dark transition-colors">LINE</a></li>
					<li><a href="#" class="hover:text-dark transition-colors">Contact</a></li>
				</ul>
			</div>
		</div>

		<!-- Bottom Bar -->
		<div class="flex flex-col md:flex-row justify-between items-center text-[10px] uppercase tracking-wider text-gray-600 border-t border-gray-300 pt-8">
			<div class="mb-4 md:mb-0">© 2025 Dunkit株式会社 (CORELAX)</div>
			<div class="flex gap-8">
				<a href="#" class="hover:text-dark transition-colors">Terms of Service</a>
				<a href="#" class="hover:text-dark transition-colors">Privacy Policy</a>
			</div>
		</div>
        
        <div class="flex justify-center mt-16 mb-8">
            <div class="flex flex-col items-center gap-2">
                <div class="text-xs text-center max-w-md leading-relaxed text-gray-600">
                    Create the future starting today.<br>
                    Building next-generation wellness infrastructure through unmanned stores.
                </div>
                <div class="mt-6 text-[10px] text-gray-500">
                    Tokyo, Minato-ku · Kawasaki, Tama Ward
                </div>
            </div>
        </div>
	</div>
</footer>

<style>
	/* Custom animations or utilities if needed */
	.animate-spin-slow {
		animation: spin 10s linear infinite;
	}
	@keyframes spin {
		from { transform: rotate(0deg); }
		to { transform: rotate(360deg); }
	}
</style>

