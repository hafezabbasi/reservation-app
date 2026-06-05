
<div class:dark={darkMode}></div>
<script>
import { onMount } from "svelte"
  import app from "./main";
const whatsappNumber = "989350657135"
const appName="Rezora"
const faAppName="رزورا"
let copyright=" © 2026 All Rights Reserved" 
let phoneNumber="09350657135"
	let showBackToTop = false

	function scrollToTop() {
		window.scrollTo({
			top: 0,
			behavior: "smooth"
		})
	}

	onMount(() => {
		const handleScroll = () => {
			showBackToTop = window.scrollY > 500
		}

		window.addEventListener("scroll", handleScroll)

		return () => {
			window.removeEventListener("scroll", handleScroll)
		}
	})
	let darkMode = false
	let menuOpen = false
const properties = [
  {
    icon: "🏨",
    title: "رزرو سریع اتاق",
    desc: "در کمتر از یک دقیقه اتاق مورد نظر خود را رزرو کنید."
  },
  {
    icon: "💳",
    title: "پرداخت امن آنلاین",
    desc: "پرداخت با درگاه‌های امن و معتبر."
  },
  {
    icon: "📅",
    title: "مدیریت رزروها",
    desc: "مشاهده، ویرایش و لغو رزرو در هر زمان."
  },
  {
    icon: "⭐",
    title: "مشاهده نظرات مهمانان",
    desc: "قبل از رزرو تجربه سایر مسافران را بخوانید."
  },
  {
    icon: "⚙️",
    title: "تعیین قوانین خاص",
    desc: "تعیین قوانین دلخواه برای مدت زمان رزرو، مبلغ اجاره و ..."
  },
  {
    icon: "🌍",
    title: "دسترسی همیشگی",
    desc: "بدون محدودیت مکانی و زمانی رزرو انجام بدید."
  }
]
	const features = [
		{
			title: "سریع مثل رعد و برق",
			desc: "برای حداکثر کارایی بهینه شده ."
		},
		{
			title: "امن",
			desc: "امنیت در سطح سازمانی."
		},
		{
			title: "آسان برای استفاده",
			desc: "مثل آب خوردن."
		}
	]

	const testimonials = [
		{
			name: "کاوه سعدی - مدیریت هتل نودشه ( مجتمع گردشگری نودشه)",
			comment: "سامانه‌ای سریع، حرفه‌ای و عالی برای مدیریت رزرواسیون، کامل و کارکرن باهاش خیلی آسونه."
		},
		
	]

	const customers = [
		"هتل نودشه",
		
	]
</script>

<svelte:body class:dark={darkMode} />
<div class:dark={darkMode}>

<div
	   class="min-h-screen  bg-white text-zinc-900 transition-colors duration-300 dark:bg-zinc-950 dark:text-white"
>

	<!-- Navbar -->
	<nav dir="ltr"
		class="sticky top-0 z-50 border-b border-zinc-200 bg-white/80 backdrop-blur-lg dark:border-zinc-800 dark:bg-zinc-950/80"
	>

		<div
			class="mx-auto flex h-16 max-w-7xl items-center justify-between px-6"
		>

			 <!-- Logo + Title -->
  <div class="flex items-center gap-3">
    
    <!-- Logo -->
    <div class="w-auto h-10">
       <a href="/">
      <img src="images/logo.png" class="h-10 w-auto" alt="{appName}">
	  </a>
    </div>

    <!-- Title -->
	  <a href="/">
    <span class="text-xl font-bold">
    {appName}
    </span>
</a>
  </div>
       
    
      

			<!-- Desktop Menu -->

			<div class="hidden items-center gap-8 md:flex">
          
        <a href="#customers">مشتری‌ها</a>
				<a href="#reviews">نظرها</a>
         <a href="#properties">خصوصیات</a>
         <a href="#features">ویژگی‌ها</a>
				
       

				<button
					on:click={() => (darkMode = !darkMode)}
					class="rounded-xl border border-zinc-300 px-4 py-2 dark:border-zinc-700"
				>
					{darkMode ? "☀️" : "🌙"}
				</button>

			</div>

			<!-- Mobile -->

			<div class="flex items-center gap-3 md:hidden">

				<button
					on:click={() => (darkMode = !darkMode)}
				>
					{darkMode ? "☀️" : "🌙"}
				</button>

				<button
					on:click={() => (menuOpen = !menuOpen)}
					class="text-2xl"
				>
					☰
				</button>

			</div>

		</div>

		{#if menuOpen}

			<div
				class="flex flex-col gap-4 border-t border-zinc-200 text-right px-6 py-4 dark:border-zinc-800 md:hidden"
			>
  <a href="#customers">مشتری‌ها</a>
				<a href="#reviews">نظرها</a>
         <a href="#properties">خصوصیات</a>
         <a href="#features">ویژگی‌ها</a>
       

			</div>

		{/if}

	</nav>

	<!-- Hero -->

	<section class="mx-auto max-w-7xl px-6 py-24">

		<div
			class="flex flex-col-reverse items-center gap-16 lg:flex-row"
		>

			<div class="flex-1 text-center lg:text-right">

				<h4 class="mt-6 text-1xl font-thin  md:text-2xl"
				>اپلیکیشن‌ِ مدیریت رزرواسیون  

				</h4>
                 
				<h1
					  class="mt-2 text-5xl font-black leading-tight md:text-7xl"
				>
					رزورا؛
					<span
						class="bg-gradient-to-r from-[#2563ff] to-[#7c3aed] bg-clip-text text-transparent"
					>
						مدیریت هوشمند، رزرو آسان
					</span>
				</h1>
           
				<ul class="list-disc pt-4 ps-6 text-lg leading-7 text-right">
        
		  <li>هوشمند، یکپارچه، همیشه در دسترس</li>
         <li>سادگی در ظاهر و کارایی،  قدرت در مدیریت </li>
         
		 <li>مناسب برای هتل، مجتمع‌ گردشگری، اقامتگاه  و ...</li>
		 <li>رزرو آنلاین </li>
       </ul>

				<div
					class="mt-10 flex flex-col gap-4 sm:flex-row"
				>
				

				</div>

			</div>

			<div class="flex-1">

				<div
					class="rounded-3xl w-auto bg-gradient-to-br bg-gradient-to-r  p-1"
				>

					<img
						src="images/logo.png"
						alt="app"
						class="rounded-3xl m-auto h-65 md:h-auto w-auto"
					/>
					

				</div>

			</div>

		</div>

	</section>

	<!-- Features -->

	<section
		id="features"
		class="bg-zinc-50 py-24 dark:bg-zinc-900"
	>

		<div class="mx-auto max-w-7xl px-6">

			<h2
				class="mb-16 text-center text-4xl font-bold"
			>
				ویژگی‌ها
			</h2>

			<div
				class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3"
			>

				{#each features as feature}

					<div
						class="rounded-3xl border border-zinc-200 text-center bg-white p-8 transition hover:-translate-y-2 dark:border-zinc-800 dark:bg-zinc-950"
					>

						<h3
							class="mb-4 text-2xl font-bold "
						>
							{feature.title}
						</h3>

						<p
							class="text-zinc-600 dark:text-zinc-400"
						>
							{feature.desc}
						</p>

					</div>

				{/each}

			</div>

		</div>

	</section>

  <section id="properties" class="py-24">

  <div class="mx-auto max-w-7xl px-6">

    <div class="text-center">

    

      <h2 class="mt-4 text-4xl font-bold">
        همه چیز برای یک رزرو آسان
      </h2>

      <p class="mt-4 text-zinc-500">
        تجربه‌ای سریع، امن و لذت‌بخش برای رزرو هتل، مجتمع گردشگری، اقامتگاه و ...
      </p>

    </div>

    <div
      class="mt-16 grid gap-8 md:grid-cols-2 lg:grid-cols-3"
    >

      {#each properties as property}

        <div
          class="group rounded-3xl border border-zinc-200 bg-white p-8 transition-all duration-300 hover:-translate-y-2 hover:shadow-xl dark:border-zinc-800 dark:bg-zinc-900"
        >

          <div
            class="mb-6 flex h-16 w-16 items-center justify-center rounded-2xl bg-cyan-500/10 text-4xl transition-transform group-hover:scale-110"
          >
            {property.icon}
          </div>

          <h3 class="mb-3 text-xl font-bold">
            {property.title}
          </h3>

          <p class="text-zinc-500">
            {property.desc}
          </p>

        </div>

      {/each}
        
    </div>

  </div>

</section>

	<!-- Customers -->

	<section
		id="customers"
		class="py-24"
	>

		<div class="mx-auto max-w-7xl px-6">

			<h2
				class="mb-16 text-center text-4xl font-bold"
			>
	       حرف ما رو قبول نکنید، از مشتری‌هامون بپرسید

			</h2>

			<div
				class="grid grid-cols-2 gap-6 md:grid-cols-3 lg:grid-cols-6"
			>

				{#each customers as customer}

					<div
						class="rounded-2xl border border-zinc-200 p-6 text-center font-bold dark:border-zinc-800 transition hover:scale-105"
					>
						<a href="https://nodeshehotel.com/" target="_blank">{customer}</a>
					</div>
        

				{/each}

			</div>

		</div>

	</section>

	<!-- Testimonials -->

	<section
		id="reviews"
		class="bg-zinc-50 py-24 dark:bg-zinc-900"
	>

		<div class="mx-auto max-w-7xl px-6">

			<h2
				class="mb-16 text-center text-4xl font-bold"
			>
			نظر مشتری
			</h2>

			<div
				class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3"
			>

				{#each testimonials as review}

					<div
						class="rounded-3xl border border-zinc-200 bg-white p-8 dark:border-zinc-800 dark:bg-zinc-950"
					>

						<p
							class="mb-6 text-zinc-600 dark:text-zinc-400"
						>
							"{review.comment}"
						</p>

						<h4
							class="font-bold"
						>
							{review.name}
						</h4>

					</div>

				{/each}

			</div>

		</div>

	</section>

	<!-- CTA -->

	
	<!-- Footer -->

	<footer
		class="border-t border-zinc-200 py-6 dark:border-zinc-800"
	>

		<div
			class="mx-auto flex max-w-7xl flex-col justify-between gap-6 px-6 md:flex-row"
		>

			<div>
		 <!-- Logo + Title -->
  <div class="flex items-center gap-3 mx-20">
    
    <!-- Logo -->
    <div class="w-auto h-10">
       <a href="/">
      <img src="images/logo.png" class="h-10 w-auto" alt="{appName}">
	  </a>
    </div>

    <!-- Title -->
	 <a href="/">
    <span class="text-xl font-bold">
    {faAppName} 

    </span>
</a>
  </div>

				<p
					class="mt-2 mx-20 text-zinc-500"
				>
					اپلیکیشن‌ِ حرفه‌ای برای تیم‌های حرفه‌ای.
				</p>

			</div>

			<p class="text-zinc-500 text-center">
				{copyright}
					
			</p>
			

		</div>

	</footer>
</div>
{#if showBackToTop}

	<button
		on:click={scrollToTop}
		class="fixed bottom-40 right-4 z-50 flex h-14 w-14 items-center justify-center rounded-full bg-gradient-to-r from-[#2563ff] to-[#7c3aed] text-xl text-white shadow-lg transition hover:scale-110"
	>
		↑
	</button>

{/if}
<!-- Phone -->
<a
	href="tel:{phoneNumber}"
	aria-label="Call us"
	class="fixed bottom-24 right-4 z-50 flex h-14 w-14 items-center justify-center rounded-full bg-blue-500 shadow-lg transition hover:scale-110"
>
	<svg
		xmlns="http://www.w3.org/2000/svg"
		viewBox="0 0 24 24"
		fill="none"
		stroke="white"
		stroke-width="2"
		stroke-linecap="round"
		stroke-linejoin="round"
		class="h-7 w-7"
	>
		<path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6A19.79 19.79 0 0 1 2.08 4.18 2 2 0 0 1 4.06 2h3a2 2 0 0 1 2 1.72c.12.9.34 1.78.65 2.62a2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.46-1.17a2 2 0 0 1 2.11-.45c.84.31 1.72.53 2.62.65A2 2 0 0 1 22 16.92z"/>
	</svg>
</a>

<!-- WhatsApp -->
<a
	href={`https://wa.me/${whatsappNumber}`}
	target="_blank"
	rel="noopener noreferrer"
	aria-label="Chat on WhatsApp"
	class="fixed bottom-6 right-4 z-50 flex h-14 w-14 items-center justify-center rounded-full bg-green-500 shadow-lg transition hover:scale-110"
>
	<svg
		xmlns="http://www.w3.org/2000/svg"
		viewBox="0 0 24 24"
		fill="white"
		class="h-8 w-8"
	>
		<path
			d="M20.52 3.48A11.86 11.86 0 0 0 12.05 0C5.5 0 .18 5.32.18 11.87c0 2.09.55 4.13 1.6 5.93L0 24l6.37-1.67a11.86 11.86 0 0 0 5.68 1.45h.01c6.55 0 11.87-5.32 11.87-11.87 0-3.17-1.24-6.14-3.41-8.43z"
		/>
	</svg>
</a>

</div>