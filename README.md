
# paypilot.github.ioimport React from "react";

const features = [
  {
    icon: "💸",
    title: "Money Routes",
    description:
      "Automatically split each paycheck into bills, savings, debt, taxes, and spending money the moment income arrives.",
  },
  {
    icon: "🛡️",
    title: "Bill Guard",
    description:
      "Protect rent, utilities, insurance, and other must-pay expenses before money is available for everyday spending.",
  },
  {
    icon: "🏦",
    title: "Goal Buckets",
    description:
      "Build emergency savings, vacation funds, and long-term goals with simple automated transfers.",
  },
  {
    icon: "💳",
    title: "Credit Coach",
    description:
      "Get personalized credit-building actions based on utilization, payment timing, and debt payoff progress.",
  },
  {
    icon: "🧾",
    title: "Tax Stash",
    description:
      "Set aside estimated taxes automatically, built for freelancers, commission workers, and side hustlers.",
  },
  {
    icon: "📊",
    title: "Safe-to-Spend",
    description:
      "See what you can actually spend after upcoming bills, savings targets, and debt obligations are accounted for.",
  },
];

const steps = [
  {
    number: "01",
    title: "Connect your income",
    description:
      "Link your account or paycheck source so PayPilot can recognize when money comes in.",
  },
  {
    number: "02",
    title: "Build your route",
    description:
      "Choose how your money should be divided across bills, savings, debt, taxes, and flexible spending.",
  },
  {
    number: "03",
    title: "Let PayPilot fly",
    description:
      "PayPilot organizes your money automatically and updates your safe-to-spend number in real time.",
  },
];

const audiences = [
  "Freelancers",
  "Commission workers",
  "Young professionals",
  "Gig workers",
  "Sales teams",
  "Students with part-time income",
];

const pricing = [
  {
    name: "Starter",
    price: "$0",
    description: "For users who want basic paycheck organization.",
    features: ["Manual money routes", "Basic safe-to-spend view", "3 goal buckets", "Bill reminders"],
    cta: "Start free",
    highlighted: false,
  },
  {
    name: "Pilot Plus",
    price: "$8",
    description: "For users who want automation and smarter planning.",
    features: ["Automatic paycheck routing", "Unlimited goal buckets", "Tax Stash", "Credit Coach", "Income smoothing"],
    cta: "Try Pilot Plus",
    highlighted: true,
  },
  {
    name: "Team",
    price: "Custom",
    description: "For employers and platforms supporting workers with variable income.",
    features: ["Employee financial wellness", "Custom onboarding", "Insights dashboard", "Dedicated support"],
    cta: "Contact sales",
    highlighted: false,
  },
];

const faqs = [
  {
    question: "Is PayPilot a bank?",
    answer:
      "No. PayPilot is a money-routing and financial planning platform designed to work with your existing accounts.",
  },
  {
    question: "Who is PayPilot best for?",
    answer:
      "PayPilot is especially useful for people with irregular or variable income, including freelancers, commission workers, gig workers, and young professionals.",
  },
  {
    question: "What makes PayPilot different from a budgeting app?",
    answer:
      "Most budgeting apps show where your money went. PayPilot helps decide where your money should go before it gets spent.",
  },
  {
    question: "Can PayPilot help build credit?",
    answer:
      "Yes. PayPilot includes credit-building tools that help users manage payment timing, reduce utilization, and organize debt payoff goals.",
  },
];

function Button({ children, variant = "primary" }) {
  const base = "inline-flex items-center justify-center rounded-full px-7 py-3 text-sm font-semibold transition";
  const styles =
    variant === "secondary"
      ? "border border-slate-700 bg-transparent text-white hover:bg-white hover:text-slate-950"
      : "bg-cyan-400 text-slate-950 hover:bg-cyan-300";

  return <button className={`${base} ${styles}`}>{children}</button>;
}

function Card({ children, className = "" }) {
  return <div className={`rounded-3xl border ${className}`}>{children}</div>;
}

export default function PayPilotLandingPage() {
  return (
    <div className="min-h-screen bg-slate-950 text-white">
      <div className="pointer-events-none absolute inset-0 overflow-hidden">
        <div className="absolute -top-40 left-1/2 h-96 w-96 -translate-x-1/2 rounded-full bg-cyan-500/20 blur-3xl" />
        <div className="absolute top-96 right-0 h-80 w-80 rounded-full bg-emerald-500/10 blur-3xl" />
        <div className="absolute bottom-0 left-0 h-80 w-80 rounded-full bg-blue-500/10 blur-3xl" />
      </div>

      <header className="relative z-10 mx-auto flex max-w-7xl items-center justify-between px-6 py-6 lg:px-8">
        <div className="flex items-center gap-3">
          <div className="flex h-11 w-11 items-center justify-center rounded-2xl bg-cyan-400 text-xl font-bold text-slate-950 shadow-lg shadow-cyan-400/20">
            ✈
          </div>
          <div>
            <p className="text-xl font-bold tracking-tight">PayPilot</p>
            <p className="text-xs text-slate-400">Automated money routing</p>
          </div>
        </div>

        <nav className="hidden items-center gap-8 text-sm text-slate-300 md:flex">
          <a href="#features" className="hover:text-white">Features</a>
          <a href="#how" className="hover:text-white">How it works</a>
          <a href="#pricing" className="hover:text-white">Pricing</a>
          <a href="#faq" className="hover:text-white">FAQ</a>
        </nav>

        <button className="rounded-full bg-white px-5 py-2 text-sm font-semibold text-slate-950 hover:bg-slate-200">
          Join waitlist
        </button>
      </header>

      <main className="relative z-10">
        <section className="mx-auto grid max-w-7xl items-center gap-14 px-6 pb-20 pt-12 lg:grid-cols-2 lg:px-8 lg:pb-28 lg:pt-20">
          <div>
            <div className="mb-6 inline-flex items-center gap-2 rounded-full border border-cyan-400/30 bg-cyan-400/10 px-4 py-2 text-sm text-cyan-200">
              <span>✨</span>
              <span>Built for variable income, bills, debt, and goals</span>
            </div>

            <h1 className="max-w-3xl text-5xl font-bold tracking-tight md:text-6xl lg:text-7xl">
              Your paycheck, autopiloted.
            </h1>

            <p className="mt-6 max-w-2xl text-lg leading-8 text-slate-300">
              PayPilot automatically routes your income toward bills, savings, taxes, debt, and credit-building goals — so every dollar has a job before you spend it.
            </p>

            <div className="mt-8 flex flex-col gap-4 sm:flex-row">
              <Button>Build my money route <span className="ml-2">→</span></Button>
              <Button variant="secondary">See how it works</Button>
            </div>

            <div className="mt-8 flex flex-wrap items-center gap-5 text-sm text-slate-400">
              <div className="flex items-center gap-2"><span className="text-emerald-400">✓</span> No spreadsheet needed</div>
              <div className="flex items-center gap-2"><span className="text-emerald-400">✓</span> Built for irregular income</div>
              <div className="flex items-center gap-2"><span className="text-emerald-400">✓</span> Clear safe-to-spend number</div>
            </div>
          </div>

          <div className="relative">
            <div className="rounded-[2rem] border border-slate-800 bg-slate-900/80 p-6 shadow-2xl shadow-cyan-950/40 backdrop-blur md:p-8">
              <div className="mb-6 flex items-center justify-between">
                <div>
                  <p className="text-sm text-slate-400">Next paycheck route</p>
                  <p className="text-3xl font-bold text-white">$2,450.00</p>
                </div>
                <div className="rounded-full bg-emerald-400/10 px-4 py-2 text-sm font-medium text-emerald-300">
                  Ready to route
                </div>
              </div>

              <div className="space-y-4">
                {[
                  ["Bills protected", "$890", "36%"],
                  ["Savings goals", "$420", "17%"],
                  ["Debt payoff", "$310", "13%"],
                  ["Tax stash", "$245", "10%"],
                  ["Safe to spend", "$585", "24%"],
                ].map(([label, amount, percent]) => (
                  <div key={label} className="rounded-2xl bg-slate-800/70 p-4">
                    <div className="mb-2 flex items-center justify-between text-sm">
                      <span className="text-slate-300">{label}</span>
                      <span className="font-semibold text-white">{amount}</span>
                    </div>
                    <div className="h-2 overflow-hidden rounded-full bg-slate-700">
                      <div className="h-full rounded-full bg-cyan-400" style={{ width: percent }} />
                    </div>
                  </div>
                ))}
              </div>

              <div className="mt-6 rounded-2xl border border-cyan-400/20 bg-cyan-400/10 p-5">
                <div className="flex items-start gap-3">
                  <span className="mt-1 text-cyan-300">🔒</span>
                  <div>
                    <p className="font-semibold text-white">Safe-to-spend updated</p>
                    <p className="mt-1 text-sm leading-6 text-slate-300">
                      After bills and goals, you have $585 available until your next paycheck.
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </section>

        <section className="border-y border-slate-800 bg-slate-900/50 px-6 py-8 lg:px-8">
          <div className="mx-auto flex max-w-7xl flex-col gap-4 text-center md:flex-row md:items-center md:justify-between md:text-left">
            <p className="text-sm uppercase tracking-[0.25em] text-slate-500">Designed for</p>
            <div className="flex flex-wrap justify-center gap-3 md:justify-end">
              {audiences.map((audience) => (
                <span key={audience} className="rounded-full border border-slate-700 px-4 py-2 text-sm text-slate-300">
                  {audience}
                </span>
              ))}
            </div>
          </div>
        </section>

        <section id="features" className="mx-auto max-w-7xl px-6 py-24 lg:px-8">
          <div className="mx-auto max-w-3xl text-center">
            <p className="text-sm font-semibold uppercase tracking-[0.25em] text-cyan-300">Features</p>
            <h2 className="mt-4 text-4xl font-bold tracking-tight md:text-5xl">
              Budgeting that acts before you spend.
            </h2>
            <p className="mt-5 text-lg leading-8 text-slate-300">
              PayPilot gives your money a flight plan before it disappears into random purchases, forgotten bills, or surprise tax payments.
            </p>
          </div>

          <div className="mt-14 grid gap-5 md:grid-cols-2 lg:grid-cols-3">
            {features.map((feature) => (
              <Card key={feature.title} className="border-slate-800 bg-slate-900/70 p-7 transition hover:-translate-y-1 hover:border-cyan-400/40 hover:bg-slate-900">
                <div className="mb-5 flex h-12 w-12 items-center justify-center rounded-2xl bg-cyan-400/10 text-2xl text-cyan-300">
                  {feature.icon}
                </div>
                <h3 className="text-xl font-semibold text-white">{feature.title}</h3>
                <p className="mt-3 leading-7 text-slate-400">{feature.description}</p>
              </Card>
            ))}
          </div>
        </section>

        <section id="how" className="bg-white px-6 py-24 text-slate-950 lg:px-8">
          <div className="mx-auto max-w-7xl">
            <div className="grid gap-12 lg:grid-cols-[0.9fr_1.1fr] lg:items-center">
              <div>
                <p className="text-sm font-semibold uppercase tracking-[0.25em] text-cyan-700">How it works</p>
                <h2 className="mt-4 text-4xl font-bold tracking-tight md:text-5xl">
                  Set the route once. Let your money follow it.
                </h2>
                <p className="mt-5 text-lg leading-8 text-slate-600">
                  PayPilot replaces constant budgeting decisions with an automated system that prioritizes the financial responsibilities that matter most.
                </p>
              </div>

              <div className="grid gap-5">
                {steps.map((step) => (
                  <div key={step.number} className="rounded-3xl border border-slate-200 bg-slate-50 p-7">
                    <div className="flex gap-5">
                      <div className="text-2xl font-bold text-cyan-700">{step.number}</div>
                      <div>
                        <h3 className="text-xl font-semibold">{step.title}</h3>
                        <p className="mt-2 leading-7 text-slate-600">{step.description}</p>
                      </div>
                    </div>
                  </div>
                ))}
              </div>
            </div>
          </div>
        </section>

        <section className="mx-auto max-w-7xl px-6 py-24 lg:px-8">
          <div className="rounded-[2rem] border border-slate-800 bg-slate-900 p-8 md:p-12 lg:p-16">
            <div className="grid gap-10 lg:grid-cols-2 lg:items-center">
              <div>
                <p className="text-sm font-semibold uppercase tracking-[0.25em] text-emerald-300">Why it matters</p>
                <h2 className="mt-4 text-4xl font-bold tracking-tight md:text-5xl">
                  Your account balance is not the same as your spending money.
                </h2>
                <p className="mt-5 text-lg leading-8 text-slate-300">
                  Seeing $1,200 in checking can feel good until rent, insurance, taxes, and credit card payments hit. PayPilot shows the number that actually matters: what is safe to spend.
                </p>
              </div>

              <div className="grid gap-4">
                {[
                  ["⏱️", "Avoid bill shock", "Upcoming expenses stay funded before flexible spending opens up."],
                  ["🧾", "Prepare for taxes", "Tax Stash helps variable-income workers avoid painful surprises."],
                  ["💳", "Improve credit habits", "Credit Coach turns payoff timing and utilization into simple actions."],
                ].map(([icon, title, description]) => (
                  <div key={title} className="flex gap-4 rounded-3xl bg-slate-800/70 p-5">
                    <div className="flex h-11 w-11 shrink-0 items-center justify-center rounded-2xl bg-emerald-400/10 text-xl text-emerald-300">
                      {icon}
                    </div>
                    <div>
                      <h3 className="font-semibold text-white">{title}</h3>
                      <p className="mt-1 leading-7 text-slate-400">{description}</p>
                    </div>
                  </div>
                ))}
              </div>
            </div>
          </div>
        </section>

        <section id="pricing" className="bg-slate-900/50 px-6 py-24 lg:px-8">
          <div className="mx-auto max-w-7xl">
            <div className="mx-auto max-w-3xl text-center">
              <p className="text-sm font-semibold uppercase tracking-[0.25em] text-cyan-300">Pricing</p>
              <h2 className="mt-4 text-4xl font-bold tracking-tight md:text-5xl">
                Start simple. Automate when you are ready.
              </h2>
            </div>

            <div className="mt-14 grid gap-6 lg:grid-cols-3">
              {pricing.map((plan) => (
                <div
                  key={plan.name}
                  className={`rounded-3xl border p-8 ${
                    plan.highlighted
                      ? "border-cyan-400 bg-cyan-400 text-slate-950 shadow-2xl shadow-cyan-950/40"
                      : "border-slate-800 bg-slate-950 text-white"
                  }`}
                >
                  {plan.highlighted && (
                    <div className="mb-5 inline-flex rounded-full bg-slate-950 px-4 py-2 text-sm font-medium text-white">
                      Most popular
                    </div>
                  )}

                  <h3 className="text-2xl font-bold">{plan.name}</h3>
                  <div className="mt-4 flex items-end gap-2">
                    <span className="text-5xl font-bold">{plan.price}</span>
                    {plan.price !== "Custom" && <span className="mb-2 text-sm opacity-70">/month</span>}
                  </div>
                  <p className="mt-4 leading-7 opacity-75">{plan.description}</p>

                  <div className="mt-7 space-y-3">
                    {plan.features.map((item) => (
                      <div key={item} className="flex items-center gap-3">
                        <span>✓</span>
                        <span>{item}</span>
                      </div>
                    ))}
                  </div>

                  <button
                    className={`mt-8 w-full rounded-full px-6 py-3 font-semibold transition ${
                      plan.highlighted
                        ? "bg-slate-950 text-white hover:bg-slate-800"
                        : "bg-white text-slate-950 hover:bg-slate-200"
                    }`}
                  >
                    {plan.cta}
                  </button>
                </div>
              ))}
            </div>
          </div>
        </section>

        <section id="faq" className="mx-auto max-w-4xl px-6 py-24 lg:px-8">
          <div className="text-center">
            <p className="text-sm font-semibold uppercase tracking-[0.25em] text-cyan-300">FAQ</p>
            <h2 className="mt-4 text-4xl font-bold tracking-tight md:text-5xl">
              Questions, cleared for takeoff.
            </h2>
          </div>

          <div className="mt-12 space-y-4">
            {faqs.map((faq) => (
              <div key={faq.question} className="rounded-3xl border border-slate-800 bg-slate-900/70 p-7">
                <h3 className="text-lg font-semibold text-white">{faq.question}</h3>
                <p className="mt-3 leading-7 text-slate-400">{faq.answer}</p>
              </div>
            ))}
          </div>
        </section>

        <section className="px-6 pb-24 lg:px-8">
          <div className="mx-auto max-w-7xl rounded-[2rem] bg-cyan-400 px-8 py-16 text-center text-slate-950 md:px-12">
            <h2 className="text-4xl font-bold tracking-tight md:text-5xl">
              Give every dollar a destination.
            </h2>
            <p className="mx-auto mt-5 max-w-2xl text-lg leading-8 text-slate-800">
              Build your first money route and see what your paycheck can do when it has a plan before it lands.
            </p>
            <button className="mt-8 rounded-full bg-slate-950 px-8 py-3 text-base font-semibold text-white hover:bg-slate-800">
              Join the PayPilot waitlist <span className="ml-2">→</span>
            </button>
          </div>
        </section>
      </main>

      <footer className="relative z-10 border-t border-slate-800 px-6 py-8 lg:px-8">
        <div className="mx-auto flex max-w-7xl flex-col gap-4 text-sm text-slate-500 md:flex-row md:items-center md:justify-between">
          <p>© 2026 PayPilot. All rights reserved.</p>
          <div className="flex gap-6">
            <a href="#" className="hover:text-slate-300">Privacy</a>
            <a href="#" className="hover:text-slate-300">Terms</a>
            <a href="#" className="hover:text-slate-300">Security</a>
          </div>
        </div>
      </footer>
    </div>
  );
}
