import React, { useState } from "react";
import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

export default function AboQahtGaming() {
  const [showForm, setShowForm] = useState(false);
  const [submissions, setSubmissions] = useState([]);
  const [form, setForm] = useState({ name: "", discord: "", server: "" });
  const [showSubmissions, setShowSubmissions] = useState(false);

  const handleSubmit = () => {
    if (!form.name || !form.discord || !form.server) {
      alert("يرجى تعبئة جميع البيانات");
      return;
    }

    setSubmissions([...submissions, { ...form, id: Date.now() }]);
    setForm({ name: "", discord: "", server: "" });
    setShowForm(false);
    alert("تم إرسال طلب الانضمام ✅");
  };

  return (
    <div className="min-h-screen bg-black text-white p-6">
      {/* Header */}
      <div className="text-center mb-12">
        <motion.h1
          className="text-5xl font-extrabold mb-4 text-purple-500"
          animate={{ scale: [1, 1.08, 1] }}
          transition={{ repeat: Infinity, duration: 2 }}
        >
          abo qaht
        </motion.h1>
        <p className="text-gray-400 text-lg">
          مجتمع ألعاب وبرمجة احترافية
        </p>

        <Button
          onClick={() => setShowForm(true)}
          className="mt-6 text-lg px-8 py-3 rounded-2xl"
        >
          انضمام إلى مجتمع abo qaht
        </Button>
      </div>

      {/* Games Section */}
      <div className="grid md:grid-cols-3 gap-6 mb-16">
        <Card className="bg-purple-900 rounded-2xl">
          <CardContent className="p-6">
            <h2 className="text-2xl font-bold mb-3 text-purple-300">FiveM</h2>
            <p className="leading-7 text-purple-100">
              تطوير سكربتات احترافية، أنظمة إدارية متقدمة، حماية سيرفر،
              وربط متكامل مع قواعد البيانات والدسكورد.
            </p>
          </CardContent>
        </Card>

        <Card className="bg-blue-900 rounded-2xl">
          <CardContent className="p-6">
            <h2 className="text-2xl font-bold mb-3 text-blue-300">Discord Systems</h2>
            <p className="leading-7 text-blue-100">
              برمجة بوتات احترافية، أنظمة لوق، إدارة رتب، حماية متقدمة
              وربط السيرفرات بأنظمة الألعاب.
            </p>
          </CardContent>
        </Card>

        <Card className="bg-green-900 rounded-2xl">
          <CardContent className="p-6">
            <h2 className="text-2xl font-bold mb-3 text-green-300">Web Development</h2>
            <p className="leading-7 text-green-100">
              تصميم مواقع حديثة وسريعة بواجهات احترافية وتجربة مستخدم
              قوية ومتجاوبة مع جميع الأجهزة.
            </p>
          </CardContent>
        </Card>
      </div>

      {/* About Me */}
      <Card className="bg-gray-900 rounded-2xl shadow-xl mb-16">
        <CardContent className="p-8">
          <h2 className="text-3xl font-bold mb-6 text-yellow-400">من أنا</h2>
          <p className="leading-8 mb-4 text-gray-300">
            أنا abo qaht، مطور متخصص في برمجة FiveM وأنظمة Discord
            الاحترافية، بالإضافة إلى تصميم وتطوير المواقع الإلكترونية.
            أركز على تقديم حلول قوية ومستقرة تخدم مجتمعات الألعاب.
          </p>
          <p className="leading-8 mb-4 text-gray-400">
            أمتلك خبرة في بناء أنظمة مخصصة بالكامل حسب الطلب، سواء كانت
            أنظمة إدارية، متاجر، حماية متقدمة، أو ربط قواعد بيانات.
          </p>
          <p className="leading-8 text-gray-500">
            هدفي هو تقديم جودة عالية، أداء قوي، ودعم فني مستمر لضمان
            نجاح أي مشروع أعمل عليه.
          </p>
        </CardContent>
      </Card>

      {/* Join Form Modal */}
      {showForm && (
        <div className="fixed inset-0 bg-black bg-opacity-70 flex items-center justify-center">
          <Card className="bg-gray-900 w-full max-w-md rounded-2xl">
            <CardContent className="p-6">
              <h2 className="text-2xl font-bold mb-4">نموذج الانضمام</h2>

              <input
                type="text"
                placeholder="اسمك"
                value={form.name}
                onChange={(e) => setForm({ ...form, name: e.target.value })}
                className="w-full p-2 mb-3 rounded text-black"
              />
              <input
                type="text"
                placeholder="اسمك في الدسكورد"
                value={form.discord}
                onChange={(e) => setForm({ ...form, discord: e.target.value })}
                className="w-full p-2 mb-3 rounded text-black"
              />
              <input
                type="text"
                placeholder="رابط سيرفرك"
                value={form.server}
                onChange={(e) => setForm({ ...form, server: e.target.value })}
                className="w-full p-2 mb-4 rounded text-black"
              />

              <div className="flex justify-between">
                <Button onClick={handleSubmit}>إرسال</Button>
                <Button onClick={() => setShowForm(false)}>إغلاق</Button>
              </div>
            </CardContent>
          </Card>
        </div>
      )}

      {/* Submissions Page */}
      <div className="text-center">
        <Button onClick={() => setShowSubmissions(!showSubmissions)}>
          عرض طلبات الانضمام
        </Button>
      </div>

      {showSubmissions && (
        <Card className="bg-gray-900 rounded-2xl shadow-xl mt-8">
          <CardContent className="p-6">
            <h2 className="text-2xl font-bold mb-4">طلبات الانضمام</h2>
            {submissions.length === 0 && <p>لا توجد طلبات حالياً</p>}
            {submissions.map((sub) => (
              <div key={sub.id} className="border-b border-gray-700 pb-3 mb-3">
                <p><strong>الاسم:</strong> {sub.name}</p>
                <p><strong>الدسكورد:</strong> {sub.discord}</p>
                <p><strong>السيرفر:</strong> {sub.server}</p>
              </div>
            ))}
          </CardContent>
        </Card>
      )}
    </div>
  );
}
