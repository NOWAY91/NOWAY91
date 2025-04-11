## Hi there 👋

<!--
**NOWAY91/NOWAY91** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
"use client"

import { useState } from "react"
import Image from "next/image"
import { Badge } from "@/components/ui/badge"
import { Button } from "@/components/ui/button"
import { Card, CardContent } from "@/components/ui/card"
import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs"
import {
  Award,
  Briefcase,
  ChevronRight,
  FileText,
  Globe,
  Mail,
  MapPin,
  Menu,
  Shield,
  Star,
  User,
  X,
} from "lucide-react"

export function ProfileWebsite() {
  const [mobileMenuOpen, setMobileMenuOpen] = useState(false)

  return (
    <div className="bg-slate-100 min-h-screen" dir="rtl">
      {/* Header */}
      <header className="bg-slate-900 text-white sticky top-0 z-50">
        <div className="container mx-auto px-4 py-3 flex justify-between items-center">
          <div className="flex items-center gap-2">
            <Shield className="h-6 w-6 text-amber-500" />
            <span className="font-bold text-lg">اللواء / محمد الخالدي</span>
          </div>

          {/* Desktop Navigation */}
          <nav className="hidden md:flex items-center gap-6">
            <a href="#profile" className="hover:text-amber-400 transition-colors">
              الملف الشخصي
            </a>
            <a href="#experience" className="hover:text-amber-400 transition-colors">
              الخبرات
            </a>
            <a href="#skills" className="hover:text-amber-400 transition-colors">
              المهارات
            </a>
            <a href="#contact" className="hover:text-amber-400 transition-colors">
              التواصل
            </a>
          </nav>

          {/* Mobile Menu Button */}
          <button className="md:hidden text-white" onClick={() => setMobileMenuOpen(!mobileMenuOpen)}>
            {mobileMenuOpen ? <X className="h-6 w-6" /> : <Menu className="h-6 w-6" />}
          </button>
        </div>

        {/* Mobile Navigation */}
        {mobileMenuOpen && (
          <nav className="md:hidden bg-slate-800 py-4 px-4 flex flex-col gap-4">
            <a
              href="#profile"
              className="hover:text-amber-400 transition-colors py-2 border-b border-slate-700"
              onClick={() => setMobileMenuOpen(false)}
            >
              الملف الشخصي
            </a>
            <a
              href="#experience"
              className="hover:text-amber-400 transition-colors py-2 border-b border-slate-700"
              onClick={() => setMobileMenuOpen(false)}
            >
              الخبرات
            </a>
            <a
              href="#skills"
              className="hover:text-amber-400 transition-colors py-2 border-b border-slate-700"
              onClick={() => setMobileMenuOpen(false)}
            >
              المهارات
            </a>
            <a
              href="#contact"
              className="hover:text-amber-400 transition-colors py-2"
              onClick={() => setMobileMenuOpen(false)}
            >
              التواصل
            </a>
          </nav>
        )}
      </header>

      {/* Hero Section */}
      <section className="bg-gradient-to-b from-slate-900 to-slate-800 text-white py-16 md:py-24">
        <div className="container mx-auto px-4 flex flex-col md:flex-row items-center gap-8">
          <div className="md:w-1/2 flex flex-col items-center md:items-end">
            <div className="relative w-48 h-48 md:w-64 md:h-64 rounded-full overflow-hidden border-4 border-amber-500 mb-6">
              <Image src="/placeholder.svg?height=256&width=256" alt="صورة شخصية" fill className="object-cover" />
              <div className="absolute bottom-0 left-0 right-0 bg-amber-500 text-center py-1 text-xs font-bold">
                لواء
              </div>
            </div>
          </div>
          <div className="md:w-1/2 text-center md:text-right">
            <Badge className="bg-amber-500 hover:bg-amber-600 mb-4">القيادي السابق</Badge>
            <h1 className="text-3xl md:text-4xl font-bold mb-4">اللواء / محمد الخالدي</h1>
            <p className="text-slate-300 mb-6 max-w-lg">
              شخصية قيادية مخضرمة عملت في أبرز السيرفرات وأكثرها تنظيمًا في عالم الرول بلاي، شغلت مناصب عليا واستشارية في
              عدة مدن افتراضية.
            </p>
            <div className="flex flex-wrap gap-3 justify-center md:justify-end">
              <Badge variant="outline" className="bg-slate-700 text-amber-400 border-amber-400">
                <MapPin className="ml-1 h-3 w-3" />
                مدينة التسعين
              </Badge>
              <Badge variant="outline" className="bg-slate-700 text-amber-400 border-amber-400">
                <Briefcase className="ml-1 h-3 w-3" />
                +5 سنوات خبرة
              </Badge>
              <Badge variant="outline" className="bg-slate-700 text-amber-400 border-amber-400">
                <Shield className="ml-1 h-3 w-3" />
                حرس الحدود
              </Badge>
            </div>
          </div>
        </div>
      </section>

      {/* Profile Section */}
      <section id="profile" className="py-16 bg-white">
        <div className="container mx-auto px-4">
          <div className="flex items-center gap-2 mb-8">
            <User className="h-6 w-6 text-amber-500" />
            <h2 className="text-2xl font-bold">الملف الشخصي</h2>
          </div>

          <Card className="border-none shadow-lg">
            <CardContent className="p-6">
              <p className="text-slate-700 leading-relaxed">
                شخصية قيادية مخضرمة عملت في أبرز السيرفرات وأكثرها تنظيمًا في عالم الرول بلاي، شغلت مناصب عليا واستشارية
                في عدة مدن افتراضية، وساهمت بشكل مباشر في تطوير البنية التحتية للقطاعات العسكرية والمدنية. يتميز
                بالصرامة في تطبيق النظام، والقدرة على إعادة هيكلة القطاعات، والخبرة العميقة في تطوير بيئات اللعب
                والأنظمة داخل السيرفرات. معروف بالحيادية التامة، والبعد عن أي مسؤوليات مالية أو إدارية خارجة عن المهام
                القيادية والتنظيمية.
              </p>

              <div className="grid grid-cols-1 md:grid-cols-3 gap-6 mt-8">
                <div className="bg-slate-50 p-4 rounded-lg">
                  <div className="flex items-center gap-2 mb-2">
                    <Badge className="bg-amber-500">الرتبة</Badge>
                  </div>
                  <p className="font-semibold">لواء</p>
                </div>

                <div className="bg-slate-50 p-4 rounded-lg">
                  <div className="flex items-center gap-2 mb-2">
                    <Badge className="bg-amber-500">المسمى الوظيفي</Badge>
                  </div>
                  <p className="font-semibold">قيادي إداري ومستشار أمني في بيئة الرول بلاي الافتراضية</p>
                </div>

                <div className="bg-slate-50 p-4 rounded-lg">
                  <div className="flex items-center gap-2 mb-2">
                    <Badge className="bg-amber-500">سنوات الخبرة</Badge>
                  </div>
                  <p className="font-semibold">أكثر من 5 سنوات في المناصب القيادية والإشرافية</p>
                </div>
              </div>
            </CardContent>
          </Card>
        </div>
      </section>

      {/* Experience Section */}
      <section id="experience" className="py-16 bg-slate-50">
        <div className="container mx-auto px-4">
          <div className="flex items-center gap-2 mb-8">
            <Briefcase className="h-6 w-6 text-amber-500" />
            <h2 className="text-2xl font-bold">الخبرات العملية</h2>
          </div>

          <div className="space-y-8">
            {/* Experience 1 */}
            <Card className="border-none shadow-lg overflow-hidden">
              <div className="bg-amber-500 h-2"></div>
              <CardContent className="p-6">
                <div className="flex flex-col md:flex-row md:items-center justify-between mb-4">
                  <div>
                    <h3 className="text-xl font-bold">مدينة التسعين رول بلاي</h3>
                    <p className="text-slate-500">الأبرز والأهم في المسيرة</p>
                  </div>
                  <Badge className="bg-slate-800 self-start md:self-center mt-2 md:mt-0">
                    نائب قائد حرس الحدود – برتبة لواء
                  </Badge>
                </div>

                <div className="space-y-4">
                  <div className="flex items-start gap-2">
                    <ChevronRight className="h-5 w-5 text-amber-500 shrink-0 mt-0.5" />
                    <p>مستشار لقائد الأمن العام (منتدب رسميًا لتحسين القطاع والقطار)</p>
                  </div>

                  <div>
                    <p className="font-medium mb-2">مُطوّر عام للمدينة من خلال:</p>
                    <ul className="space-y-2">
                      <li className="flex items-start gap-2">
                        <ChevronRight className="h-5 w-5 text-amber-500 shrink-0 mt-0.5" />
                        <p>تحديث كامل لجميع المركبات في القطاعات العسكرية والمدنية</p>
                      </li>
                      <li className="flex items-start gap-2">
                        <ChevronRight className="h-5 w-5 text-amber-500 shrink-0 mt-0.5" />
                        <p>تحسين شامل للمابات داخل المدينة</p>
                      </li>
                      <li className="flex items-start gap-2">
                        <ChevronRight className="h-5 w-5 text-amber-500 shrink-0 mt-0.5" />
                        <p>تطوير وتصميم ملابس مخصصة للقطاعات العسكرية والمدنية</p>
                      </li>
                      <li className="flex items-start gap-2">
                        <ChevronRight className="h-5 w-5 text-amber-500 shrink-0 mt-0.5" />
                        <p>رفع كفاءة الأداء العام للمدينة وتحسين التجربة للمواطنين واللاعبين</p>
                      </li>
                    </ul>
                  </div>

                  <div className="bg-red-50 border border-red-100 rounded-lg p-4 mt-4">
                    <p className="font-medium text-red-800 mb-2">سبب الاستقالة:</p>
                    <p className="text-red-700">
                      رغم الجهود الضخمة التي قُدمت، تم تقديم استقالتي بسبب تفشي الظلم، وسوء تعامل بعض الإداريين، بالإضافة
                      إلى التجاوزات الإدارية والمالية التي أثّرت على مصداقية المدينة وأدّت إلى نفور اللاعبين. ورغم محاولات
                      التواصل العديدة من بعض القيادات لإعادتي، رفضت الرجوع بشكل قاطع حفاظًا على موقفي ومبادئي.
                    </p>
                  </div>
                </div>
              </CardContent>
            </Card>

            {/* Experience 2 */}
            <Card className="border-none shadow-lg overflow-hidden">
              <div className="bg-slate-600 h-2"></div>
              <CardContent className="p-6">
                <div className="flex flex-col md:flex-row md:items-center justify-between mb-4">
                  <div>
                    <h3 className="text-xl font-bold">سيرفر شارع الستين رول بلاي</h3>
                  </div>
                  <Badge className="bg-slate-700 self-start md:self-center mt-2 md:mt-0">إداري برتبة "أدمن بلس"</Badge>
                </div>

                <div className="space-y-4">
                  <ul className="space-y-2">
                    <li className="flex items-start gap-2">
                      <ChevronRight className="h-5 w-5 text-slate-500 shrink-0 mt-0.5" />
                      <p>إشراف كامل على التنظيم الإداري، وتحديث الأنظمة والقوانين</p>
                    </li>
                    <li className="flex items-start gap-2">
                      <ChevronRight className="h-5 w-5 text-slate-500 shrink-0 mt-0.5" />
                      <p>
                        لا علاقة لي بأي مسؤوليات مالية داخل السيرفر، حيث كان الجانب المالي بالكامل تحت إشراف مالك
                        السيرفر
                      </p>
                    </li>
                  </ul>

                  <div className="bg-blue-50 border border-blue-100 rounded-lg p-4 mt-4">
                    <p className="font-medium text-blue-800 mb-2">سبب الإغلاق:</p>
                    <p className="text-blue-700">
                      لم تُكتب للمدينة الاستمرارية، وكان السبب الأهم هو الظروف الصحية التي يعاني منها مالك السيرفر "أخونا
                      جبل"، مما أدى إلى تعليق المشروع رغم الإمكانيات التنظيمية العالية.
                    </p>
                  </div>
                </div>
              </CardContent>
            </Card>

            {/* Experience 3 */}
            <Card className="border-none shadow-lg overflow-hidden">
              <div className="bg-slate-600 h-2"></div>
              <CardContent className="p-6">
                <div className="flex flex-col md:flex-row md:items-center justify-between mb-4">
                  <div>
                    <h3 className="text-xl font-bold">مدينة الثريا رول بلاي</h3>
                  </div>
                  <Badge className="bg-slate-700 self-start md:self-center mt-2 md:mt-0">
                    مستشار للقائد الأعلى للأمن الدبلوماسي
                  </Badge>
                </div>

                <div className="space-y-4">
                  <ul className="space-y-2">
                    <li className="flex items-start gap-2">
                      <ChevronRight className="h-5 w-5 text-slate-500 shrink-0 mt-0.5" />
                      <p>برتبة راهو رايد</p>
                    </li>
                    <li className="flex items-start gap-2">
                      <ChevronRight className="h-5 w-5 text-slate-500 shrink-0 mt-0.5" />
                      <p>
                        شاركت ضمن الصفوف القيادية العليا ولكن لم يُمنح لي المجال الكافي لإبراز إمكانياتي أو تطوير القطاع
                      </p>
                    </li>
                  </ul>

                  <div className="bg-blue-50 border border-blue-100 rounded-lg p-4 mt-4">
                    <p className="font-medium text-blue-800 mb-2">سبب الاستقالة:</p>
                    <p className="text-blue-700">
                      عدم التقدير الكافي من بعض القيادات، وعدم وجود بيئة داعمة لتفعيل المبادرات التنظيمية.
                    </p>
                  </div>
                </div>
              </CardContent>
            </Card>

            {/* Experience 4 */}
            <Card className="border-none shadow-lg overflow-hidden">
              <div className="bg-slate-600 h-2"></div>
              <CardContent className="p-6">
                <div className="flex flex-col md:flex-row md:items-center justify-between mb-4">
                  <div>
                    <h3 className="text-xl font-bold">مدينة 91 رول بلاي</h3>
                  </div>
                  <Badge className="bg-slate-700 self-start md:self-center mt-2 md:mt-0">إداري برتبة "أدمن بلس"</Badge>
                </div>

                <div className="space-y-4">
                  <ul className="space-y-2">
                    <li className="flex items-start gap-2">
                      <ChevronRight className="h-5 w-5 text-slate-500 shrink-0 mt-0.5" />
                      <p>شاركت في المراحل التأسيسية للسيرفر</p>
                    </li>
                  </ul>

                  <div className="bg-blue-50 border border-blue-100 rounded-lg p-4 mt-4">
                    <p className="font-medium text-blue-800 mb-2">سبب المغادرة:</p>
                    <p className="text-blue-700">
                      بسبب حداثة السيرفر وضعف أعداد اللاعبين، بالإضافة إلى تخبطات في القوانين وعدم توفر الصلاحيات
                      الكاملة التي تمكنني من بناء استراتيجية تنظيمية واضحة.
                    </p>
                  </div>
                </div>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      {/* Skills Section */}
      <section id="skills" className="py-16 bg-white">
        <div className="container mx-auto px-4">
          <div className="flex items-center gap-2 mb-8">
            <Star className="h-6 w-6 text-amber-500" />
            <h2 className="text-2xl font-bold">المهارات والاهتمامات</h2>
          </div>

          <Tabs defaultValue="skills" className="w-full">
            <TabsList className="grid w-full grid-cols-2 mb-8">
              <TabsTrigger value="skills">المهارات</TabsTrigger>
              <TabsTrigger value="interests">الاهتمامات</TabsTrigger>
            </TabsList>

            <TabsContent value="skills">
              <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
                <Card className="border-none shadow-lg">
                  <CardContent className="p-6">
                    <div className="flex items-center gap-3 mb-4">
                      <div className="bg-amber-100 p-2 rounded-full">
                        <FileText className="h-5 w-5 text-amber-600" />
                      </div>
                      <h3 className="font-bold">تطوير شامل للقطاعات</h3>
                    </div>
                    <p className="text-slate-600">مركبات – ملابس – مابات</p>
                  </CardContent>
                </Card>

                <Card className="border-none shadow-lg">
                  <CardContent className="p-6">
                    <div className="flex items-center gap-3 mb-4">
                      <div className="bg-amber-100 p-2 rounded-full">
                        <Shield className="h-5 w-5 text-amber-600" />
                      </div>
                      <h3 className="font-bold">القيادة والإشراف على الأنظمة الأمنية</h3>
                    </div>
                    <p className="text-slate-600">إدارة وتنظيم القطاعات الأمنية بكفاءة عالية</p>
                  </CardContent>
                </Card>

                <Card className="border-none shadow-lg">
                  <CardContent className="p-6">
                    <div className="flex items-center gap-3 mb-4">
                      <div className="bg-amber-100 p-2 rounded-full">
                        <FileText className="h-5 w-5 text-amber-600" />
                      </div>
                      <h3 className="font-bold">صياغة قوانين وسياسات عامة للسيرفرات</h3>
                    </div>
                    <p className="text-slate-600">وضع أطر تنظيمية واضحة تضمن سير العمل بشكل سلس</p>
                  </CardContent>
                </Card>

                <Card className="border-none shadow-lg">
                  <CardContent className="p-6">
                    <div className="flex items-center gap-3 mb-4">
                      <div className="bg-amber-100 p-2 rounded-full">
                        <User className="h-5 w-5 text-amber-600" />
                      </div>
                      <h3 className="font-bold">التوجيه الاستشاري للقيادات</h3>
                    </div>
                    <p className="text-slate-600">تقديم الاستشارات والتوجيهات للقيادات العليا</p>
                  </CardContent>
                </Card>

                <Card className="border-none shadow-lg">
                  <CardContent className="p-6">
                    <div className="flex items-center gap-3 mb-4">
                      <div className="bg-amber-100 p-2 rounded-full">
                        <Briefcase className="h-5 w-5 text-amber-600" />
                      </div>
                      <h3 className="font-bold">التنظيم الإداري والرقابي</h3>
                    </div>
                    <p className="text-slate-600">وضع هياكل إدارية فعالة وأنظمة رقابية دقيقة</p>
                  </CardContent>
                </Card>

                <Card className="border-none shadow-lg">
                  <CardContent className="p-6">
                    <div className="flex items-center gap-3 mb-4">
                      <div className="bg-amber-100 p-2 rounded-full">
                        <Mail className="h-5 w-5 text-amber-600" />
                      </div>
                      <h3 className="font-bold">التواصل الفعّال مع الفرق التنفيذية والإدارية</h3>
                    </div>
                    <p className="text-slate-600">بناء جسور تواصل فعالة بين مختلف المستويات الإدارية</p>
                  </CardContent>
                </Card>
              </div>
            </TabsContent>

            <TabsContent value="interests">
              <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
                <Card className="border-none shadow-lg">
                  <CardContent className="p-6">
                    <div className="flex items-center gap-3 mb-4">
                      <div className="bg-slate-100 p-2 rounded-full">
                        <Globe className="h-5 w-5 text-slate-600" />
                      </div>
                      <h3 className="font-bold">تحسين بيئة اللعب الجماعية</h3>
                    </div>
                    <p className="text-slate-600">ضمن إطار احترافي ومنظم يعزز تجربة اللاعبين</p>
                  </CardContent>
                </Card>

                <Card className="border-none shadow-lg">
                  <CardContent className="p-6">
                    <div className="flex items-center gap-3 mb-4">
                      <div className="bg-slate-100 p-2 rounded-full">
                        <Shield className="h-5 w-5 text-slate-600" />
                      </div>
                      <h3 className="font-bold">رفع جودة القطاعات العسكرية والمدنية</h3>
                    </div>
                    <p className="text-slate-600">داخل السيرفرات من خلال التطوير المستمر</p>
                  </CardContent>
                </Card>

                <Card className="border-none shadow-lg">
                  <CardContent className="p-6">
                    <div className="flex items-center gap-3 mb-4">
                      <div className="bg-slate-100 p-2 rounded-full">
                        <Award className="h-5 w-5 text-slate-600" />
                      </div>
                      <h3 className="font-bold">تأسيس بيئات افتراضية قائمة على احترام القوانين</h3>
                    </div>
                    <p className="text-slate-600">والعدالة الإدارية بين جميع الأطراف</p>
                  </CardContent>
                </Card>

                <Card className="border-none shadow-lg">
                  <CardContent className="p-6">
                    <div className="flex items-center gap-3 mb-4">
                      <div className="bg-slate-100 p-2 rounded-full">
                        <User className="h-5 w-5 text-slate-600" />
                      </div>
                      <h3 className="font-bold">تعزيز تجربة اللاعبين</h3>
                    </div>
                    <p className="text-slate-600">من خلال الأنظمة الحديثة والمطورة</p>
                  </CardContent>
                </Card>
              </div>
            </TabsContent>
          </Tabs>
        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="py-16 bg-slate-900 text-white">
        <div className="container mx-auto px-4">
          <div className="flex items-center gap-2 mb-8">
            <Mail className="h-6 w-6 text-amber-500" />
            <h2 className="text-2xl font-bold">التواصل</h2>
          </div>

          <div className="max-w-xl mx-auto">
            <Card className="bg-slate-800 border-none shadow-lg">
              <CardContent className="p-6">
                <p className="text-slate-300 mb-6 text-center">
                  للتواصل معي بخصوص الاستشارات الإدارية أو المناصب القيادية في سيرفرات الرول بلاي، يرجى ملء النموذج
                  أدناه:
                </p>

                <form className="space-y-4">
                  <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <div className="space-y-2">
                      <label htmlFor="name" className="text-sm font-medium text-slate-300">
                        الاسم
                      </label>
                      <input
                        type="text"
                        id="name"
                        className="w-full px-3 py-2 bg-slate-700 border border-slate-600 rounded-md focus:outline-none focus:ring-2 focus:ring-amber-500"
                        placeholder="أدخل اسمك"
                      />
                    </div>
                    <div className="space-y-2">
                      <label htmlFor="email" className="text-sm font-medium text-slate-300">
                        البريد الإلكتروني
                      </label>
                      <input
                        type="email"
                        id="email"
                        className="w-full px-3 py-2 bg-slate-700 border border-slate-600 rounded-md focus:outline-none focus:ring-2 focus:ring-amber-500"
                        placeholder="أدخل بريدك الإلكتروني"
                      />
                    </div>
                  </div>

                  <div className="space-y-2">
                    <label htmlFor="subject" className="text-sm font-medium text-slate-300">
                      الموضوع
                    </label>
                    <input
                      type="text"
                      id="subject"
                      className="w-full px-3 py-2 bg-slate-700 border border-slate-600 rounded-md focus:outline-none focus:ring-2 focus:ring-amber-500"
                      placeholder="موضوع الرسالة"
                    />
                  </div>

                  <div className="space-y-2">
                    <label htmlFor="message" className="text-sm font-medium text-slate-300">
                      الرسالة
                    </label>
                    <textarea
                      id="message"
                      rows={4}
                      className="w-full px-3 py-2 bg-slate-700 border border-slate-600 rounded-md focus:outline-none focus:ring-2 focus:ring-amber-500"
                      placeholder="اكتب رسالتك هنا..."
                    ></textarea>
                  </div>

                  <Button className="w-full bg-amber-500 hover:bg-amber-600 text-white">إرسال الرسالة</Button>
                </form>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-slate-950 text-slate-400 py-8">
        <div className="container mx-auto px-4 text-center">
          <div className="flex justify-center items-center gap-2 mb-4">
            <Shield className="h-5 w-5 text-amber-500" />
            <span className="font-bold text-white">اللواء / محمد الخالدي</span>
          </div>
          <p className="mb-4">القيادي السابق في بيئة الرول بلاي الافتراضية</p>
          <div className="flex justify-center gap-4 mb-6">
            <a href="#" className="hover:text-amber-400 transition-colors">
              <svg className="h-5 w-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                <path
                  fillRule="evenodd"
                  d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z"
                  clipRule="evenodd"
                />
              </svg>
            </a>
            <a href="#" className="hover:text-amber-400 transition-colors">
              <svg className="h-5 w-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                <path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84" />
              </svg>
            </a>
            <a href="#" className="hover:text-amber-400 transition-colors">
              <svg className="h-5 w-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                <path
                  fillRule="evenodd"
                  d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"
                  clipRule="evenodd"
                />
              </svg>
            </a>
          </div>
          <p className="text-xs">© 2023 جميع الحقوق محفوظة</p>
        </div>
      </footer>
    </div>
  )
}
