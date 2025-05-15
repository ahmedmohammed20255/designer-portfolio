<div class="max-w-xl mx-auto p-6 bg-white rounded-xl shadow-md mt-8 border border-gray-200">
  <h2 class="text-2xl font-bold mb-6 text-center text-gray-800">طرق الدفع</h2>

  <div class="mb-6 space-y-3">
    <p class="text-lg font-semibold">البنك: راجحي</p>
    <p>رقم الحساب: <span class="font-mono">077010110006084281691</span></p>
  </div>

  <form id="paymentReceiptForm" class="space-y-4" enctype="multipart/form-data" method="POST" action="/submit-payment">
    <div>
      <label for="name" class="block mb-1 font-semibold text-gray-700">الاسم الكامل</label>
      <input type="text" id="name" name="name" required placeholder="أدخل اسمك الكامل"
        class="w-full border border-gray-300 rounded-md p-2 focus:outline-none focus:ring-2 focus:ring-green-500" />
    </div>

    <div>
      <label for="phone" class="block mb-1 font-semibold text-gray-700">رقم الجوال</label>
      <input type="tel" id="phone" name="phone" required placeholder="أدخل رقم جوالك"
        class="w-full border border-gray-300 rounded-md p-2 focus:outline-none focus:ring-2 focus:ring-green-500" />
    </div>

    <div>
      <label for="paymentReceipt" class="block mb-1 font-semibold text-gray-700">تحميل إيصال الدفع</label>
      <input type="file" id="paymentReceipt" name="paymentReceipt" accept="image/*,application/pdf" required
        class="w-full border border-gray-300 rounded-md p-2 focus:outline-none focus:ring-2 focus:ring-green-500" />
      <p class="text-xs text-gray-500 mt-1">يمكنك رفع صورة أو ملف PDF للإيصال.</p>
    </div>

    <div class="text-center">
      <button type="submit"
        class="bg-green-600 hover:bg-green-700 text-white font-bold py-2 px-6 rounded-xl transition-all">
        إرسال الإيصال
      </button>
    </div>
  </form>
</div>

<script>
  document.getElementById('paymentReceiptForm').addEventListener('submit', function(event) {
    const fileInput = document.getElementById('paymentReceipt');
    if (!fileInput.value) {
      event.preventDefault();
      alert('الرجاء رفع إيصال الدفع قبل الإرسال.');
    }
  });
</script>
