<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>🔥 TikTok ব্যাচ ডাউনলোডার | ভিডিও + সব ছবি স্লাইডশো ডাউনলোড</title>

    <style>
        *{
            margin:0;
            padding:0;
            box-sizing:border-box;
            font-family:'Poppins',system-ui,-apple-system,'Segoe UI',Roboto,sans-serif;
        }

        body{
            background:#0d0d0d;
            color:#fff;
            display:flex;
            justify-content:center;
            align-items:center;
            min-height:100vh;
            padding:20px;
        }

        .container{
            width:100%;
            max-width:650px;
            background:#1c1c1c;
            padding:24px 22px;
            border-radius:28px;
            box-shadow:0 20px 35px rgba(0,0,0,.5);
            border:1px solid rgba(255,255,255,.05);
        }

        h2{
            text-align:center;
            color:#ff0050;
            font-weight:700;
            letter-spacing:-0.3px;
            font-size:1.8rem;
            margin-bottom:8px;
            display:flex;
            align-items:center;
            justify-content:center;
            gap:8px;
        }

        .sub{
            text-align:center;
            font-size:.8rem;
            color:#aaa;
            margin-bottom:20px;
            border-bottom:1px dashed #333;
            padding-bottom:8px;
        }

        .input-wrapper{
            position:relative;
            width:100%;
        }

        input{
            width:100%;
            padding:14px 16px;
            border-radius:16px;
            border:none;
            outline:none;
            margin-top:8px;
            background:#2a2a2a;
            color:white;
            font-size:.95rem;
            transition:.2s;
            padding-right:50px;
        }

        input:focus{
            background:#333;
            box-shadow:0 0 0 2px #ff0050;
        }

        .clear-btn{
            position:absolute;
            right:12px;
            top:50%;
            transform:translateY(-50%);
            background:#ff0050;
            border:none;
            width:32px;
            height:32px;
            border-radius:30px;
            display:flex;
            align-items:center;
            justify-content:center;
            cursor:pointer;
            font-weight:bold;
            font-size:18px;
            color:white;
            transition:.1s;
            opacity:.7;
        }

        .clear-btn:hover{
            opacity:1;
        }

        .auto-badge{
            text-align:center;
            font-size:.7rem;
            color:#00f2ea;
            margin-top:8px;
        }

        .stats{
            margin-top:20px;
            background:#2a2a2a;
            padding:16px;
            border-radius:20px;
            display:none;
            border:1px solid #3a3a3a;
        }

        .stats p{
            margin:8px 0;
            display:flex;
            align-items:center;
            gap:12px;
            flex-wrap:wrap;
            font-size:.9rem;
        }

        .stats strong{
            color:#00f2ea;
            min-width:85px;
        }

        .hashtag-section{
            background:#1e1e1e;
            border-radius:18px;
            padding:12px 14px;
            margin:12px 0 6px;
            border-left:4px solid #ff0050;
        }

        .hashtags-list{
            display:flex;
            flex-wrap:wrap;
            gap:8px;
            align-items:center;
        }

        .hashtag-chip{
            background:#2c2c2c;
            padding:6px 14px;
            border-radius:40px;
            font-size:.8rem;
            color:#00f2ea;
            cursor:pointer;
            display:inline-flex;
            align-items:center;
            gap:6px;
            border:1px solid #3f3f3f;
        }

        .copy-toast{
            position:fixed;
            bottom:30px;
            left:50%;
            transform:translateX(-50%);
            background:#1f1f1f;
            color:#00f2ea;
            padding:8px 20px;
            border-radius:40px;
            font-size:.8rem;
            z-index:999;
            backdrop-filter:blur(12px);
            border:1px solid #ff0050;
            opacity:0;
            transition:.2s;
            pointer-events:none;
        }

        video{
            width:100%;
            border-radius:20px;
            margin-top:20px;
            background:#000;
            max-height:480px;
            object-fit:contain;
        }

        .downloads{
            display:flex;
            gap:12px;
            margin-top:16px;
            flex-wrap:wrap;
        }

        .downloads a{
            flex:1;
            text-align:center;
            padding:12px 8px;
            border-radius:40px;
            text-decoration:none;
            font-weight:bold;
            font-size:.9rem;
        }

        .video-btn{
            background:#00c853;
            color:white;
        }

        .audio-btn{
            background:#2979ff;
            color:white;
        }

        .image-download-btn{
            background:#ff6d00;
            color:white;
            display:flex;
            align-items:center;
            justify-content:center;
            gap:6px;
        }

        .loading{
            text-align:center;
            margin-top:20px;
            color:#00f2ea;
            display:none;
            font-weight:500;
        }

        .gallery-section{
            margin-top:20px;
            background:#252525;
            border-radius:20px;
            padding:16px;
            display:none;
        }

        .gallery-title{
            font-weight:bold;
            margin-bottom:12px;
            color:#ffaa00;
            display:flex;
            align-items:center;
            gap:10px;
            flex-wrap:wrap;
            justify-content:space-between;
        }

        .gallery-grid{
            display:grid;
            grid-template-columns:repeat(auto-fill,minmax(100px,1fr));
            gap:12px;
            max-height:320px;
            overflow-y:auto;
            padding:4px;
        }

        .gallery-item{
            background:#1e1e1e;
            border-radius:14px;
            overflow:hidden;
            text-align:center;
            padding:8px;
            transition:.1s;
            border:1px solid #3a3a3a;
        }

        .gallery-item img{
            width:100%;
            aspect-ratio:1/1;
            object-fit:cover;
            border-radius:12px;
            cursor:pointer;
        }

        .gallery-item button{
            background:#ff0050;
            border:none;
            margin-top:8px;
            padding:6px;
            border-radius:30px;
            font-size:.7rem;
            font-weight:bold;
            cursor:pointer;
            color:white;
            width:100%;
        }

        .download-all-btn{
            background:linear-gradient(135deg,#ff6d00,#ff0050);
            border:none;
            padding:8px 18px;
            border-radius:40px;
            color:white;
            font-weight:bold;
            cursor:pointer;
            font-size:.8rem;
        }

        .image-row{
            display:flex;
            align-items:center;
            gap:12px;
            margin-top:12px;
            flex-wrap:wrap;
        }

        hr{
            border-color:#333;
            margin:12px 0;
        }
    </style>
</head>

<body>

<div class="container">

    <h2>🔥 TikTok অল-ইন-ওয়ান ডাউনলোডার</h2>

    <div class="sub">
        📹 ভিডিও · 🖼️ ছবি স্লাইডশো · 🎵 অডিও · #হ্যাশট্যাগ কপি
    </div>

    <div class="input-wrapper">
        <input type="text" id="url"
        placeholder="TikTok লিংক পেস্ট করুন (ভিডিও বা ছবি অটো শনাক্ত হবে)"
        spellcheck="false">

        <button class="clear-btn" id="clearBtn">✖</button>
    </div>

    <div class="auto-badge">
        ⚡ অটো শনাক্ত: ভিডিও / ছবি স্লাইডশো (সব ছবি ডাউনলোড করা যাবে)
    </div>

    <div class="loading" id="loading">
        ⏳ TikTok থেকে তথ্য আনা হচ্ছে...
    </div>

    <div class="stats" id="stats">
        <p><strong>👁 ভিউ:</strong> <span id="views"></span></p>
        <p><strong>❤️ লাইক:</strong> <span id="likes"></span></p>
        <p><strong>💬 কমেন্ট:</strong> <span id="comments"></span></p>
        <p><strong>🎤 লেখক:</strong> <span id="author" style="cursor:pointer;" title="কপি করতে ক্লিক করুন"></span></p>

        <div class="hashtag-section" id="hashtagContainer" style="display:none;">
            <div class="hashtags-list" id="hashtagsList"></div>
        </div>
    </div>

    <video id="video" controls preload="metadata"></video>

    <div class="image-row" id="imageRow" style="display:none;">
        <a id="downloadImageBtn" class="image-download-btn" download>
            🖼️ কভার ছবি ডাউনলোড
        </a>
    </div>

    <div class="gallery-section" id="gallerySection">

        <div class="gallery-title">
            <span>📸 ছবির গ্যালারি</span>

            <button id="downloadAllImagesBtn" class="download-all-btn">
                ⬇️ সব ছবি ZIP আকারে ডাউনলোড
            </button>
        </div>

        <div class="gallery-grid" id="galleryGrid"></div>

        <p style="font-size:.7rem;margin-top:10px;color:#aaa;">
            💡 প্রতিটি ছবিতে ক্লিক করে আলাদাভাবে সংরক্ষণ করতে পারবেন
        </p>

    </div>

    <div class="downloads" id="downloads" style="display:none;">
        <a id="videoDownload" class="video-btn" download>
            📥 ভিডিও ডাউনলোড
        </a>

        <a id="audioDownload" class="audio-btn" download>
            🎧 অডিও ডাউনলোড
        </a>
    </div>

</div>

<div id="toastMessage" class="copy-toast">✅ কপি হয়েছে!</div>

<script src="https://cdn.jsdelivr.net/npm/jszip@3.10.1/dist/jszip.min.js"></script>

<script>

function showToast(msg){
    const toast=document.getElementById('toastMessage');
    toast.textContent=msg || '✅ সম্পন্ন!';
    toast.style.opacity='1';

    setTimeout(()=>{
        toast.style.opacity='0';
    },2000);
}

async function copyToClipboard(text){
    try{
        await navigator.clipboard.writeText(text);

        showToast(`📋 কপি হয়েছে`);
    }catch{
        showToast('❌ কপি করা যায়নি');
    }
}

function extractHashtags(apiData){
    let tags=[];

    if(apiData.challenges && Array.isArray(apiData.challenges)){
        tags=apiData.challenges.map(ch=>ch.title).filter(Boolean);
    }

    return [...new Set(tags)];
}

function renderHashtags(tags){

    const container=document.getElementById('hashtagContainer');
    const list=document.getElementById('hashtagsList');

    if(!tags.length){
        container.style.display='none';
        return;
    }

    container.style.display='block';
    list.innerHTML='';

    tags.forEach(tag=>{

        const chip=document.createElement('div');

        chip.className='hashtag-chip';

        chip.innerHTML=`#${tag} 📋`;

        chip.onclick=()=>copyToClipboard(`#${tag}`);

        list.appendChild(chip);
    });
}

function resetUI(){

    document.getElementById('stats').style.display='none';
    document.getElementById('downloads').style.display='none';
    document.getElementById('imageRow').style.display='none';
    document.getElementById('gallerySection').style.display='none';

    document.getElementById('video').src='';

    document.getElementById('galleryGrid').innerHTML='';
}

</script>

</body>
</html>
