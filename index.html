import React, { useState, useRef, useEffect } from 'react';
import { Send, Sparkles, User, Loader2, Plus, MessageSquare, Menu, X, Settings, ChevronDown, Zap, Brain, Flame, Lock, Mail, ArrowRight, Image as ImageIcon, Copy, Check, Terminal, Volume2, Square, Globe } from 'lucide-react';

// Firebase Imports
import { initializeApp } from 'firebase/app';
import { getAuth, signInAnonymously, signInWithCustomToken, onAuthStateChanged } from 'firebase/auth';
import { getFirestore, collection, doc, setDoc, onSnapshot } from 'firebase/firestore';

// --- Firebase Initialization ---
const firebaseConfig = typeof __firebase_config !== 'undefined' ? JSON.parse(__firebase_config) : {};
const app = initializeApp(firebaseConfig);
const auth = getAuth(app);
const db = getFirestore(app);
const appId = typeof __app_id !== 'undefined' ? __app_id : 'default-app-id';

// --- UI TRANSLATIONS DICTIONARY ---
const UI_STRINGS = {
  English: {
    subtitle: "Smart Scripting & Vision", nameOpt: "NAME (OPTIONAL)", yourName: "Your Name", email: "EMAIL", password: "PASSWORD", auth: "Authenticate", reg: "Register", needAcc: "Need an account? Create one", hasAcc: "Already registered? Sign in", resetAcc: "Want to reset your account? Register here", newChat: "New Chat", history: "History", loggedIn: "Logged In", settings: "Settings & Voice", logout: "Log Out", synced: "Cloud Synced", little: "Little Squeeze", big: "Big Squeeze", spicy: "Spicy Squeeze", ask: "Ask LEMUN for code, images, or answers...", footer: "LEMUN CORE v2.5 • STRICT AUTHENTICATION ACTIVE", lang: "Language", voice: "Voice Model", base: "Base Instructions", cancel: "Cancel", save: "Save Changes", loading: "Loading...", read: "Read Aloud", stop: "Stop Audio", painting: "Painting masterpiece...", squeezing: "Squeezing some ideas...", copied: "Copied!", copy: "Copy", script: "script", init: "Initialization complete. I am LEMUN. Welcome back,", errAuth: "Incorrect email or password.", errNoAcc: "No account found. Please register first.", errPwd: "Password must be at least 4 characters.", errErr: "An error occurred. Please try again.", initCore: "Initializing Core...", imgCleared: "Image context cleared for session performance."
  },
  Spanish: {
    subtitle: "Scripts Inteligentes y Visión", nameOpt: "NOMBRE (OPCIONAL)", yourName: "Tu Nombre", email: "CORREO", password: "CONTRASEÑA", auth: "Autenticar", reg: "Registrar", needAcc: "¿Sin cuenta? Crea una", hasAcc: "¿Ya registrado? Inicia sesión", resetAcc: "¿Restablecer cuenta? Regístrate", newChat: "Nuevo Chat", history: "Historial", loggedIn: "Conectado", settings: "Ajustes y Voz", logout: "Salir", synced: "Sincronizado", little: "Little Squeeze", big: "Big Squeeze", spicy: "Spicy Squeeze", ask: "Pide a LEMUN código, imágenes o respuestas...", footer: "LEMUN CORE v2.5 • AUTENTICACIÓN ESTRICTA", lang: "Idioma", voice: "Modelo de Voz", base: "Instrucciones Base", cancel: "Cancelar", save: "Guardar Cambios", loading: "Cargando...", read: "Leer en Voz Alta", stop: "Detener Audio", painting: "Pintando obra maestra...", squeezing: "Exprimiendo ideas...", copied: "¡Copiado!", copy: "Copiar", script: "script", init: "Inicialización completa. Soy LEMUN. Bienvenido,", errAuth: "Correo o contraseña incorrectos.", errNoAcc: "No se encontró cuenta. Regístrate primero.", errPwd: "La contraseña debe tener 4+ caracteres.", errErr: "Ocurrió un error. Intenta de nuevo.", initCore: "Inicializando Núcleo...", imgCleared: "Contexto de imagen borrado por rendimiento."
  },
  French: {
    subtitle: "Scripting Intelligent & Vision", nameOpt: "NOM (FACULTATIF)", yourName: "Votre Nom", email: "E-MAIL", password: "MOT DE PASSE", auth: "S'authentifier", reg: "S'inscrire", needAcc: "Besoin d'un compte ? Créer un", hasAcc: "Déjà inscrit ? Connectez-vous", resetAcc: "Réinitialiser ? Inscrivez-vous ici", newChat: "Nouveau Chat", history: "Historique", loggedIn: "Connecté", settings: "Paramètres & Voix", logout: "Déconnexion", synced: "Synchronisé", little: "Little Squeeze", big: "Big Squeeze", spicy: "Spicy Squeeze", ask: "Demandez à LEMUN du code, des images...", footer: "LEMUN CORE v2.5 • AUTHENTIFICATION STRICTE", lang: "Langue", voice: "Modèle Vocal", base: "Instructions de Base", cancel: "Annuler", save: "Enregistrer", loading: "Chargement...", read: "Lire à Haute Voix", stop: "Arrêter l'Audio", painting: "Peinture d'un chef-d'œuvre...", squeezing: "Pressage d'idées...", copied: "Copié !", copy: "Copier", script: "script", init: "Initialisation terminée. Je suis LEMUN. Bienvenue,", errAuth: "E-mail ou mot de passe incorrect.", errNoAcc: "Aucun compte trouvé. Veuillez vous inscrire.", errPwd: "Le mot de passe doit contenir 4+ caractères.", errErr: "Une erreur est survenue.", initCore: "Initialisation du Cœur...", imgCleared: "Contexte d'image effacé pour les performances."
  },
  German: {
    subtitle: "Intelligentes Scripting & Vision", nameOpt: "NAME (OPTIONAL)", yourName: "Dein Name", email: "E-MAIL", password: "PASSWORT", auth: "Authentifizieren", reg: "Registrieren", needAcc: "Kein Konto? Erstellen", hasAcc: "Schon registriert? Anmelden", resetAcc: "Konto zurücksetzen? Hier registrieren", newChat: "Neuer Chat", history: "Verlauf", loggedIn: "Eingeloggt", settings: "Einstellungen & Stimme", logout: "Abmelden", synced: "Cloud-Synchronisiert", little: "Little Squeeze", big: "Big Squeeze", spicy: "Spicy Squeeze", ask: "Frage LEMUN nach Code, Bildern...", footer: "LEMUN CORE v2.5 • STRIKTE AUTHENTIFIZIERUNG", lang: "Sprache", voice: "Stimmenmodell", base: "Basis-Anweisungen", cancel: "Abbrechen", save: "Speichern", loading: "Wird geladen...", read: "Vorlesen", stop: "Audio stoppen", painting: "Meisterwerk wird gemalt...", squeezing: "Ideen werden gepresst...", copied: "Kopiert!", copy: "Kopieren", script: "Skript", init: "Initialisierung abgeschlossen. Ich bin LEMUN. Willkommen,", errAuth: "Falsche E-Mail oder falsches Passwort.", errNoAcc: "Kein Konto gefunden. Bitte registrieren.", errPwd: "Passwort muss 4+ Zeichen lang sein.", errErr: "Ein Fehler ist aufgetreten.", initCore: "Kern wird initialisiert...", imgCleared: "Bildkontext aus Leistungsgründen gelöscht."
  },
  Italian: {
    subtitle: "Scripting Intelligente & Visione", nameOpt: "NOME (OPZIONALE)", yourName: "Il Tuo Nome", email: "EMAIL", password: "PASSWORD", auth: "Autentica", reg: "Registrati", needAcc: "Nessun account? Creane uno", hasAcc: "Già registrato? Accedi", resetAcc: "Vuoi reimpostare? Registrati qui", newChat: "Nuova Chat", history: "Cronologia", loggedIn: "Connesso", settings: "Impostazioni e Voce", logout: "Esci", synced: "Sincronizzato", little: "Little Squeeze", big: "Big Squeeze", spicy: "Spicy Squeeze", ask: "Chiedi a LEMUN codice, immagini...", footer: "LEMUN CORE v2.5 • AUTENTICAZIONE RIGOROSA", lang: "Lingua", voice: "Modello Vocale", base: "Istruzioni di Base", cancel: "Annulla", save: "Salva", loading: "Caricamento...", read: "Leggi ad alta voce", stop: "Ferma Audio", painting: "Dipingendo capolavoro...", squeezing: "Spremendo idee...", copied: "Copiato!", copy: "Copia", script: "script", init: "Inizializzazione completata. Sono LEMUN. Benvenuto,", errAuth: "Email o password errati.", errNoAcc: "Nessun account. Registrati prima.", errPwd: "La password deve avere 4+ caratteri.", errErr: "Si è verificato un errore.", initCore: "Inizializzazione Core...", imgCleared: "Contesto immagine cancellato per le prestazioni."
  },
  Portuguese: {
    subtitle: "Scripts Inteligentes e Visão", nameOpt: "NOME (OPCIONAL)", yourName: "Seu Nome", email: "E-MAIL", password: "SENHA", auth: "Autenticar", reg: "Registrar", needAcc: "Sem conta? Crie uma", hasAcc: "Já registrado? Entrar", resetAcc: "Redefinir conta? Registre-se", newChat: "Novo Chat", history: "Histórico", loggedIn: "Conectado", settings: "Configurações e Voz", logout: "Sair", synced: "Sincronizado", little: "Little Squeeze", big: "Big Squeeze", spicy: "Spicy Squeeze", ask: "Peça a LEMUN código, imagens ou respostas...", footer: "LEMUN CORE v2.5 • AUTENTICAÇÃO ESTRITA", lang: "Idioma", voice: "Modelo de Voz", base: "Instruções Base", cancel: "Cancelar", save: "Salvar", loading: "Carregando...", read: "Ler em voz alta", stop: "Parar Áudio", painting: "Pintando obra-prima...", squeezing: "Espremendo ideias...", copied: "Copiado!", copy: "Copiar", script: "script", init: "Inicialização concluída. Sou LEMUN. Bem-vindo,", errAuth: "E-mail ou senha incorretos.", errNoAcc: "Nenhuma conta. Registre-se primeiro.", errPwd: "A senha deve ter 4+ caracteres.", errErr: "Ocorreu um erro.", initCore: "Inicializando Núcleo...", imgCleared: "Contexto de imagem apagado pelo desempenho."
  },
  Japanese: {
    subtitle: "スマートスクリプト＆ビジョン", nameOpt: "名前（省略可）", yourName: "あなたの名前", email: "メールアドレス", password: "パスワード", auth: "認証", reg: "登録", needAcc: "アカウントを作成", hasAcc: "すでに登録済み？ログイン", resetAcc: "リセットする？ここで登録", newChat: "新しいチャット", history: "履歴", loggedIn: "ログイン中", settings: "設定と音声", logout: "ログアウト", synced: "クラウド同期済", little: "Little Squeeze", big: "Big Squeeze", spicy: "Spicy Squeeze", ask: "LEMUNにコードや画像を尋ねる...", footer: "LEMUN CORE v2.5 • 厳格な認証が有効", lang: "言語", voice: "音声モデル", base: "基本命令", cancel: "キャンセル", save: "保存", loading: "読み込み中...", read: "読み上げる", stop: "音声を停止", painting: "傑作を描画中...", squeezing: "アイデアを絞り出し中...", copied: "コピーしました！", copy: "コピー", script: "スクリプト", init: "初期化完了。私はLEMUNです。おかえりなさい、", errAuth: "メールまたはパスワードが間違っています。", errNoAcc: "アカウントがありません。先に登録してください。", errPwd: "パスワードは4文字以上です。", errErr: "エラーが発生しました。", initCore: "コアを初期化中...", imgCleared: "パフォーマンスのため画像のコンテキストを消去しました。"
  },
  Korean: {
    subtitle: "스마트 스크립팅 및 비전", nameOpt: "이름 (선택)", yourName: "당신의 이름", email: "이메일", password: "비밀번호", auth: "인증", reg: "가입", needAcc: "계정이 필요하신가요? 만들기", hasAcc: "이미 가입하셨나요? 로그인", resetAcc: "계정을 초기화하시겠습니까? 등록", newChat: "새 채팅", history: "기록", loggedIn: "로그인됨", settings: "설정 및 음성", logout: "로그아웃", synced: "클라우드 동기화됨", little: "Little Squeeze", big: "Big Squeeze", spicy: "Spicy Squeeze", ask: "LEMUN에게 코드, 이미지 또는 답변을 요청하세요...", footer: "LEMUN CORE v2.5 • 엄격한 인증 활성화됨", lang: "언어", voice: "음성 모델", base: "기본 지침", cancel: "취소", save: "저장", loading: "로딩 중...", read: "소리 내어 읽기", stop: "오디오 중지", painting: "명작을 그리는 중...", squeezing: "아이디어를 짜내는 중...", copied: "복사됨!", copy: "복사", script: "스크립트", init: "초기화 완료. 저는 LEMUN입니다. 다시 오신 것을 환영합니다, ", errAuth: "이메일 또는 비밀번호가 잘못되었습니다.", errNoAcc: "계정이 없습니다. 먼저 가입하세요.", errPwd: "비밀번호는 4자 이상이어야 합니다.", errErr: "오류가 발생했습니다.", initCore: "코어 초기화 중...", imgCleared: "성능을 위해 이미지 컨텍스트가 지워졌습니다."
  },
  Arabic: {
    subtitle: "البرمجة الذكية والرؤية", nameOpt: "الاسم (اختياري)", yourName: "اسمك", email: "البريد الإلكتروني", password: "كلمة المرور", auth: "مصادقة", reg: "تسجيل", needAcc: "ليس لديك حساب؟ أنشئ واحداً", hasAcc: "مسجل بالفعل؟ تسجيل الدخول", resetAcc: "تريد إعادة تعيين حسابك؟ سجل هنا", newChat: "محادثة جديدة", history: "السجل", loggedIn: "متصل", settings: "الإعدادات والصوت", logout: "تسجيل الخروج", synced: "مزامنة سحابية", little: "Little Squeeze", big: "Big Squeeze", spicy: "Spicy Squeeze", ask: "اسأل LEMUN عن الرمز، أو الصور...", footer: "LEMUN CORE v2.5 • مصادقة صارمة نشطة", lang: "اللغة", voice: "نموذج الصوت", base: "التعليمات الأساسية", cancel: "إلغاء", save: "حفظ", loading: "جاري التحميل...", read: "اقرأ بصوت عالٍ", stop: "إيقاف الصوت", painting: "جاري رسم تحفة...", squeezing: "عصر الأفكار...", copied: "تم النسخ!", copy: "نسخ", script: "سكربت", init: "اكتملت التهيئة. أنا LEMUN. مرحباً بعودتك، ", errAuth: "البريد الإلكتروني أو كلمة المرور غير صحيحة.", errNoAcc: "لم يتم العثور على حساب. يرجى التسجيل أولاً.", errPwd: "يجب أن تكون كلمة المرور 4 أحرف على الأقل.", errErr: "حدث خطأ. يرجى المحاولة مرة أخرى.", initCore: "جاري تهيئة النواة...", imgCleared: "تم مسح سياق الصورة من أجل الأداء."
  }
};

// --- WAV Conversion Utility for TTS ---
function createWavBlob(base64Pcm, sampleRate) {
  const binaryString = window.atob(base64Pcm);
  const len = binaryString.length;
  const bytes = new Uint8Array(len);
  for (let i = 0; i < len; i++) {
    bytes[i] = binaryString.charCodeAt(i);
  }

  const buffer = new ArrayBuffer(44 + bytes.length);
  const view = new DataView(buffer);

  const writeString = (offset, string) => {
    for (let i = 0; i < string.length; i++) {
      view.setUint8(offset + i, string.charCodeAt(i));
    }
  };

  writeString(0, 'RIFF');
  view.setUint32(4, 36 + bytes.length, true);
  writeString(8, 'WAVE');
  writeString(12, 'fmt ');
  view.setUint32(16, 16, true);
  view.setUint16(20, 1, true);
  view.setUint16(22, 1, true); 
  view.setUint32(24, sampleRate, true);
  view.setUint32(28, sampleRate * 2, true); 
  view.setUint16(32, 2, true); 
  view.setUint16(34, 16, true); 
  writeString(36, 'data');
  view.setUint32(40, bytes.length, true);

  new Uint8Array(buffer, 44).set(bytes);
  return new Blob([buffer], { type: 'audio/wav' });
}

// --- Custom Icons ---
const LemonIcon = ({ size = 24, className = "" }) => (
  <svg width={size} height={size} viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round" className={className}>
    <path d="M6 18c-2.3-2.3-3.1-6.2-1.8-9 1.4-2.8 4.7-4.1 7.8-4.1 3.1 0 6.4 1.3 7.8 4.1 1.3 2.8.5 6.7-1.8 9-2.3 2.3-6.2 2.3-12 0z" />
  </svg>
);

// --- Code Block Component ---
const CodeBlock = ({ code, language, t }) => {
  const [copied, setCopied] = useState(false);

  const handleCopy = () => {
    const textArea = document.createElement("textarea");
    textArea.value = code;
    document.body.appendChild(textArea);
    textArea.select();
    try {
      document.execCommand('copy');
      setCopied(true);
      setTimeout(() => setCopied(false), 2000);
    } catch (err) {
      console.error('Fallback copy failed', err);
    }
    document.body.removeChild(textArea);
  };

  return (
    <div className="my-4 rounded-xl overflow-hidden border border-yellow-200 shadow-sm">
      <div className="bg-yellow-900 px-4 py-2 flex justify-between items-center">
        <div className="flex items-center space-x-2">
          <Terminal size={14} className="text-amber-400" />
          <span className="text-xs font-mono text-yellow-100 uppercase tracking-wider">{language || t('script')}</span>
        </div>
        <button 
          onClick={handleCopy}
          className="text-yellow-300 hover:text-white transition-colors flex items-center space-x-1 text-xs"
        >
          {copied ? <Check size={14} className="text-green-400" /> : <Copy size={14} />}
          <span>{copied ? t('copied') : t('copy')}</span>
        </button>
      </div>
      <div className="bg-yellow-950 p-4 overflow-x-auto">
        <pre className="text-sm font-mono text-yellow-50/90 leading-relaxed whitespace-pre">
          {code}
        </pre>
      </div>
    </div>
  );
};

// --- Message Parser Component ---
const MessageContent = ({ text, t }) => {
  if (!text) return null;

  const parts = text.split(/(```[\s\S]*?```)/g);

  return (
    <div className="space-y-1">
      {parts.map((part, index) => {
        if (part.startsWith('```')) {
          const match = part.match(/```(\w+)?\n?([\s\S]*?)```/);
          if (match) {
            const language = match[1] || '';
            const code = match[2].trim();
            return <CodeBlock key={index} code={code} language={language} t={t} />;
          }
        }
        
        return (
          <div key={index} className="whitespace-pre-wrap text-yellow-950">
            {part.split('\n').map((line, i) => (
              <p key={i} className={line.trim() === '' ? 'h-2' : ''}>
                {line.split(/(\*\*.*?\*\*)/g).map((subPart, j) => {
                  if (subPart.startsWith('**') && subPart.endsWith('**')) {
                    return <strong key={j} className="font-bold text-yellow-950">{subPart.slice(2, -2)}</strong>;
                  }
                  return subPart;
                })}
              </p>
            ))}
          </div>
        );
      })}
    </div>
  );
};

// --- Custom Select Dropdown Component ---
const CustomSelect = ({ value, onChange, options, label, icon: Icon }) => {
  const [isOpen, setIsOpen] = useState(false);
  const dropdownRef = useRef(null);

  useEffect(() => {
    const handleClickOutside = (event) => {
      if (dropdownRef.current && !dropdownRef.current.contains(event.target)) {
        setIsOpen(false);
      }
    };
    document.addEventListener("mousedown", handleClickOutside);
    return () => document.removeEventListener("mousedown", handleClickOutside);
  }, []);

  return (
    <div className="space-y-2" ref={dropdownRef}>
      {label && (
        <label className="flex items-center text-xs font-bold text-yellow-600 uppercase tracking-widest">
          {Icon && <Icon size={14} className="mr-1.5" />} {label}
        </label>
      )}
      <div className="relative">
        <button
          type="button"
          onClick={() => setIsOpen(!isOpen)}
          className="w-full p-3 bg-yellow-50 border border-yellow-200 rounded-xl text-sm text-yellow-950 focus:ring-2 focus:ring-amber-400 outline-none transition-all flex justify-between items-center shadow-sm"
        >
          <span className="font-medium">{options.find(opt => opt.value === value)?.label || value}</span>
          <ChevronDown size={16} className={`text-yellow-600 transition-transform ${isOpen ? 'rotate-180' : ''}`} />
        </button>
        {isOpen && (
          <div className="absolute z-50 w-full mt-2 bg-white border border-yellow-200 rounded-xl shadow-xl overflow-hidden animate-in fade-in slide-in-from-top-2">
            <div className="max-h-48 overflow-y-auto custom-scrollbar">
              {options.map((opt) => (
                <button
                  key={opt.value}
                  type="button"
                  onClick={() => {
                    onChange(opt.value);
                    setIsOpen(false);
                  }}
                  className={`w-full text-left px-4 py-3 text-sm transition-colors ${
                    value === opt.value
                      ? 'bg-amber-100 text-amber-950 font-bold border-l-2 border-amber-500'
                      : 'text-yellow-800 hover:bg-yellow-50 font-medium border-l-2 border-transparent'
                  }`}
                >
                  {opt.label}
                </button>
              ))}
            </div>
          </div>
        )}
      </div>
    </div>
  );
};

export default function App() {
  const [firebaseUser, setFirebaseUser] = useState(null);
  const [accountData, setAccountData] = useState(null);
  const [isAuthenticated, setIsAuthenticated] = useState(false);
  const [isAuthChecking, setIsAuthChecking] = useState(true);
  
  const [isLoginView, setIsLoginView] = useState(false);
  const [email, setEmail] = useState('');
  const [password, setPassword] = useState('');
  const [authName, setAuthName] = useState('');
  const [authError, setAuthError] = useState('');
  const [isAuthLoading, setIsAuthLoading] = useState(false);

  const [chats, setChats] = useState([]);
  const [activeChatId, setActiveChatId] = useState(null);
  const [isSidebarOpen, setIsSidebarOpen] = useState(true);
  
  const defaultPrompt = "You are LEMUN, a bright, cheerful, and highly intelligent AI. Your current interface has a fresh, bright 'Yellow' theme. Your responses should be helpful, concise, slightly witty, and have a warm tone. You excel at generating code, scripts, and creative ideas.";
  const [systemPrompt, setSystemPrompt] = useState(defaultPrompt);
  const [isSettingsOpen, setIsSettingsOpen] = useState(false);
  const [tempPrompt, setTempPrompt] = useState(systemPrompt);
  
  const [ttsVoice, setTtsVoice] = useState('Kore');
  const [tempTtsVoice, setTempTtsVoice] = useState(ttsVoice);
  const [aiLanguage, setAiLanguage] = useState('English');
  const [tempAiLanguage, setTempAiLanguage] = useState(aiLanguage);

  const [activeMode, setActiveMode] = useState('little');
  const [isModeMenuOpen, setIsModeMenuOpen] = useState(false);
  const [input, setInput] = useState('');
  const [isLoading, setIsLoading] = useState(false);
  const [loadingText, setLoadingText] = useState('...');
  const [error, setError] = useState(null);
  const messagesEndRef = useRef(null);

  const audioRef = useRef(null);
  const [playingIndex, setPlayingIndex] = useState(null);
  const [isTTSLoading, setIsTTSLoading] = useState(null);

  const activeChat = chats.find(c => c.id === activeChatId) || { messages: [], title: 'Loading...' };

  // Dynamic Translation Function
  const t = (key) => UI_STRINGS[aiLanguage]?.[key] || UI_STRINGS['English'][key];

  const fetchWithRetry = async (url, options, retries = 5) => {
    const delays = [1000, 2000, 4000, 8000, 16000];
    for (let i = 0; i < retries; i++) {
      try {
        const res = await fetch(url, options);
        if (!res.ok) throw new Error(`HTTP ${res.status}`);
        return await res.json();
      } catch (err) {
        if (i === retries - 1) throw err;
        await new Promise(r => setTimeout(r, delays[i]));
      }
    }
  };

  const handleTTS = async (text, index) => {
    if (playingIndex === index && audioRef.current) {
      audioRef.current.pause();
      audioRef.current = null;
      setPlayingIndex(null);
      return;
    }
    if (audioRef.current) {
      audioRef.current.pause();
      audioRef.current = null;
      setPlayingIndex(null);
    }
    setIsTTSLoading(index);
    try {
      const apiKey = ""; 
      const url = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-tts:generateContent?key=${apiKey}`;
      
      const payload = {
        contents: [{ parts: [{ text: text }] }],
        generationConfig: {
          responseModalities: ["AUDIO"],
          speechConfig: { voiceConfig: { prebuiltVoiceConfig: { voiceName: ttsVoice } } }
        },
        model: "gemini-2.5-flash-preview-tts"
      };

      const result = await fetchWithRetry(url, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(payload)
      });

      const inlineData = result.candidates?.[0]?.content?.parts?.[0]?.inlineData;
      if (inlineData) {
        let sampleRate = 24000;
        const rateMatch = inlineData.mimeType.match(/rate=(\d+)/);
        if (rateMatch) sampleRate = parseInt(rateMatch[1], 10);

        const wavBlob = createWavBlob(inlineData.data, sampleRate);
        const wavUrl = URL.createObjectURL(wavBlob);
        
        const audio = new Audio(wavUrl);
        audioRef.current = audio;
        
        audio.onended = () => {
          setPlayingIndex(null);
          URL.revokeObjectURL(wavUrl);
        };
        
        setPlayingIndex(index);
        audio.play();
      }
    } catch (err) {
      console.error("TTS failed:", err);
    } finally {
      setIsTTSLoading(null);
    }
  };

  useEffect(() => {
    const initAuth = async () => {
      try {
        if (typeof __initial_auth_token !== 'undefined' && __initial_auth_token) {
          await signInWithCustomToken(auth, __initial_auth_token);
        } else {
          await signInAnonymously(auth);
        }
      } catch (err) {
        console.error("Auth error:", err);
      }
    };
    initAuth();
    const unsubscribe = onAuthStateChanged(auth, setFirebaseUser);
    return () => unsubscribe();
  }, []);

  useEffect(() => {
    if (!firebaseUser) return;
    
    const profileRef = doc(db, 'artifacts', appId, 'users', firebaseUser.uid, 'account', 'profile');
    const unsubscribe = onSnapshot(profileRef, (docSnap) => {
      if (docSnap.exists()) {
        const data = docSnap.data();
        setAccountData(data);
        if (data.settings) {
          setTtsVoice(data.settings.voice || 'Kore');
          setAiLanguage(data.settings.language || 'English');
          setSystemPrompt(data.settings.prompt || defaultPrompt);
        }
        if (data.isLoggedIn) {
          setIsAuthenticated(true);
        } else {
          setIsAuthenticated(false);
          setIsLoginView(true);
        }
      } else {
        setAccountData(null);
        setIsAuthenticated(false);
        setIsLoginView(false); 
      }
      setIsAuthChecking(false);
    }, (err) => {
      setIsAuthChecking(false);
    });

    return () => unsubscribe();
  }, [firebaseUser]);

  const handleAuthSubmit = async (e) => {
    e.preventDefault();
    setAuthError('');
    setIsAuthLoading(true);

    try {
      const formattedEmail = email.toLowerCase().trim();
      const profileRef = doc(db, 'artifacts', appId, 'users', firebaseUser.uid, 'account', 'profile');

      if (!isLoginView) {
        if (password.length < 4) {
          setAuthError(t('errPwd'));
          setIsAuthLoading(false);
          return;
        }
        await setDoc(profileRef, {
          email: formattedEmail,
          password: password,
          name: authName || 'User',
          isLoggedIn: true,
          settings: { voice: 'Kore', language: 'English', prompt: defaultPrompt } 
        });
        setEmail('');
        setPassword('');
        setAuthName('');
      } else {
        if (!accountData) {
          setAuthError(t('errNoAcc'));
        } else if (formattedEmail === accountData.email && password === accountData.password) {
          await setDoc(profileRef, { isLoggedIn: true }, { merge: true });
          setEmail('');
          setPassword('');
        } else {
          setAuthError(t('errAuth'));
        }
      }
    } catch (err) {
      setAuthError(t('errErr'));
    } finally {
      setIsAuthLoading(false);
    }
  };

  const handleLogOut = async () => {
    if (!firebaseUser) return;
    try {
      if (audioRef.current) { audioRef.current.pause(); audioRef.current = null; }
      setPlayingIndex(null);
      const profileRef = doc(db, 'artifacts', appId, 'users', firebaseUser.uid, 'account', 'profile');
      await setDoc(profileRef, { isLoggedIn: false }, { merge: true });
      setChats([]);
      setActiveChatId(null);
    } catch (error) {
      console.error('Error signing out:', error);
    }
  };

  const serializeMessages = (msgs) => {
    return JSON.stringify(msgs.map(m => ({
      role: m.role, text: m.text, image: m.image ? "[IMAGE_PLACEHOLDER]" : undefined
    })));
  };

  useEffect(() => {
    if (!firebaseUser || !isAuthenticated) return;
    const chatsRef = collection(db, 'artifacts', appId, 'users', firebaseUser.uid, 'chats');
    const unsubscribe = onSnapshot(chatsRef, (snapshot) => {
      const loadedChats = [];
      snapshot.forEach(doc => {
        const data = doc.data();
        let parsedMessages = [];
        try { parsedMessages = data.messagesJson ? JSON.parse(data.messagesJson) : (data.messages || []); } catch (e) {}
        loadedChats.push({ id: doc.id, title: data.title || t('newChat'), createdAt: data.createdAt || 0, messages: parsedMessages });
      });
      loadedChats.sort((a, b) => b.createdAt - a.createdAt);
      setChats(prev => loadedChats.map(lc => {
        const pc = prev.find(p => p.id === lc.id);
        if (pc) {
          lc.messages = lc.messages.map((m, i) => (m.image === "[IMAGE_PLACEHOLDER]" && pc.messages[i]?.image?.startsWith('data:image')) ? { ...m, image: pc.messages[i].image } : m);
        }
        return lc;
      }));
      setActiveChatId(curr => !curr && loadedChats.length > 0 ? loadedChats[0].id : curr);
      if (loadedChats.length === 0) createNewChatInDB(firebaseUser.uid);
    });
    return () => unsubscribe();
  }, [firebaseUser, isAuthenticated]);

  const createNewChatInDB = async (uid) => {
    const newId = Date.now().toString();
    const initial = [{ role: 'model', text: `${t('init')} ${accountData?.name || 'User'}!` }];
    await setDoc(doc(db, 'artifacts', appId, 'users', uid, 'chats', newId), {
      title: t('newChat'), messagesJson: serializeMessages(initial), createdAt: Date.now()
    });
    setActiveChatId(newId);
  };

  const handleNewChat = () => {
    if (firebaseUser) createNewChatInDB(firebaseUser.uid);
    if (window.innerWidth < 768) setIsSidebarOpen(false);
  };

  const switchChat = (id) => {
    setActiveChatId(id);
    if (window.innerWidth < 768) setIsSidebarOpen(false);
  };

  useEffect(() => { messagesEndRef.current?.scrollIntoView({ behavior: 'smooth' }); }, [activeChat?.messages, isLoading]);

  const handleSendMessage = async (e) => {
    e.preventDefault();
    if (!input.trim() || isLoading || !firebaseUser || !activeChatId) return;

    if (audioRef.current) {
      audioRef.current.pause();
      audioRef.current = null;
      setPlayingIndex(null);
    }

    const userText = input.trim();
    const newUserMsg = { role: 'user', text: userText };
    const updatedMsgs = [...activeChat.messages, newUserMsg];
    const newTitle = activeChat.messages.length <= 1 ? userText.slice(0, 24) + '...' : activeChat.title;

    setChats(prev => prev.map(c => c.id === activeChatId ? { ...c, title: newTitle, messages: updatedMsgs } : c));
    const chatRef = doc(db, 'artifacts', appId, 'users', firebaseUser.uid, 'chats', activeChatId);
    await setDoc(chatRef, { title: newTitle, messagesJson: serializeMessages(updatedMsgs) }, { merge: true });
    
    setInput('');
    setIsLoading(true);
    setLoadingText(t('squeezing'));
    setError(null);

    try {
      const apiKey = "";
      const url = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;
      
      const modeInstr = {
        little: "Fast and concise.",
        big: "Detailed and structured.",
        spicy: "Deep expert reasoning."
      };

      const imgInstr = `CRITICAL BEHAVIORAL RULE:
1. You have an image generator. To use it, you MUST include <IMAGE_PROMPT>detailed visual description</IMAGE_PROMPT> in your output.
2. ONLY generate an image if the user's LATEST message explicitly asks to see, draw, or generate a picture.
3. DO NOT repeat previous image prompts or code blocks. If the user asks a follow up question (like "what is 1+1"), just answer the question. Do not keep generating the previous image or code!`;

      const langInstr = `[CRITICAL REQUIREMENT: YOU MUST COMMUNICATE AND TRANSLATE ALL OF YOUR THOUGHTS, RESPONSES, AND OUTPUT EXCLUSIVELY INTO THIS LANGUAGE: ${aiLanguage}. However, NEVER translate your name "LEMUN". "LEMUN" is a proper noun. Always keep it exactly as "LEMUN" in all languages.]`;

      const payload = {
        contents: updatedMsgs.map((m, idx) => {
          let apiText = m.text || "Task completed.";
          if (idx === updatedMsgs.length - 1 && m.role === 'user' && aiLanguage !== 'English') {
            apiText += `\n\n[SYSTEM DIRECTIVE: You MUST process this request and respond exclusively in ${aiLanguage}. Do not reply in English. Do NOT translate the name LEMUN.]`;
          }
          return { role: m.role, parts: [{ text: apiText }] };
        }),
        systemInstruction: { parts: [{ text: `${systemPrompt}\n\n${imgInstr}\n\n${langInstr}\n\nMODE: ${modeInstr[activeMode]}` }] }
      };

      const result = await fetchWithRetry(url, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify(payload) });
      let aiText = result.candidates?.[0]?.content?.parts?.[0]?.text || "I'm sorry, I couldn't process that.";
      let base64 = null;

      const imgMatch = aiText.match(/<IMAGE_PROMPT>([\s\S]*?)<\/IMAGE_PROMPT>/i);
      if (imgMatch) {
        setLoadingText(t('painting'));
        const prompt = imgMatch[1].trim();
        aiText = aiText.replace(/<IMAGE_PROMPT>[\s\S]*?<\/IMAGE_PROMPT>/i, '').trim() || t('painting');
        
        const imgRes = await fetchWithRetry(`https://generativelanguage.googleapis.com/v1beta/models/imagen-4.0-generate-001:predict?key=${apiKey}`, {
          method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify({ instances: { prompt }, parameters: { sampleCount: 1 } })
        });
        base64 = imgRes.predictions?.[0]?.bytesBase64Encoded;
      }

      const aiMsg = { role: 'model', text: aiText, image: base64 ? `data:image/png;base64,${base64}` : undefined };
      const finalMsgs = [...updatedMsgs, aiMsg];
      
      setChats(prev => prev.map(c => c.id === activeChatId ? { ...c, messages: finalMsgs } : c));
      await setDoc(chatRef, { messagesJson: serializeMessages(finalMsgs) }, { merge: true });

    } catch (err) {
      setError(t('errErr'));
    } finally {
      setIsLoading(false);
    }
  };

  // --- FULL SCREEN LOADING ---
  if (isAuthChecking) {
    return (
      <div className="min-h-screen bg-yellow-50 flex items-center justify-center flex-col space-y-4">
        <Loader2 size={40} className="animate-spin text-amber-500" />
        <p className="text-yellow-600 text-sm font-bold tracking-widest uppercase">{t('initCore')}</p>
      </div>
    );
  }

  // --- LOGIN / REGISTER UI ---
  if (!isAuthenticated) {
    return (
      <div className="min-h-screen bg-yellow-100 flex items-center justify-center p-4">
        <div className="bg-white/90 backdrop-blur p-8 rounded-3xl shadow-xl border border-yellow-200 w-full max-w-md animate-in fade-in zoom-in-95 duration-500">
          <div className="flex flex-col items-center mb-8">
            <div className="bg-amber-400 p-4 rounded-2xl shadow-lg mb-4">
              <LemonIcon size={48} className="text-yellow-950" />
            </div>
            <h1 className="text-3xl font-extrabold text-yellow-900">LEMUN</h1>
            <p className="text-yellow-600 font-medium tracking-widest uppercase text-xs mt-1">{t('subtitle')}</p>
          </div>

          {authError && (
            <div className="mb-4 p-3 bg-red-50 border border-red-200 rounded-xl text-red-600 text-sm font-medium text-center animate-in fade-in">
              {authError}
            </div>
          )}

          <form onSubmit={handleAuthSubmit} className="space-y-4">
            {!isLoginView && (
              <div className="space-y-1 animate-in fade-in">
                <label className="text-xs font-bold text-yellow-600 ml-1">{t('nameOpt')}</label>
                <div className="relative">
                  <User className="absolute left-3 top-3 text-yellow-500" size={18} />
                  <input 
                    type="text" 
                    value={authName}
                    onChange={(e) => setAuthName(e.target.value)}
                    placeholder={t('yourName')}
                    className="w-full bg-yellow-50 border border-yellow-200 rounded-xl py-3 pl-10 pr-4 outline-none focus:ring-2 focus:ring-amber-400/50 transition-all text-yellow-950 placeholder-yellow-600/50" 
                  />
                </div>
              </div>
            )}
            <div className="space-y-1">
              <label className="text-xs font-bold text-yellow-600 ml-1">{t('email')}</label>
              <div className="relative">
                <Mail className="absolute left-3 top-3 text-yellow-500" size={18} />
                <input 
                  type="email" 
                  value={email}
                  onChange={(e) => setEmail(e.target.value)}
                  required 
                  placeholder="you@example.com" 
                  className="w-full bg-yellow-50 border border-yellow-200 rounded-xl py-3 pl-10 pr-4 outline-none focus:ring-2 focus:ring-amber-400/50 transition-all text-yellow-950 placeholder-yellow-600/50" 
                />
              </div>
            </div>
            <div className="space-y-1">
              <label className="text-xs font-bold text-yellow-600 ml-1">{t('password')}</label>
              <div className="relative">
                <Lock className="absolute left-3 top-3 text-yellow-500" size={18} />
                <input 
                  type="password" 
                  value={password}
                  onChange={(e) => setPassword(e.target.value)}
                  required 
                  placeholder="••••••••" 
                  className="w-full bg-yellow-50 border border-yellow-200 rounded-xl py-3 pl-10 pr-4 outline-none focus:ring-2 focus:ring-amber-400/50 transition-all text-yellow-950 placeholder-yellow-600/50" 
                />
              </div>
            </div>
            <button 
              type="submit" 
              disabled={isAuthLoading || !email || !password}
              className="w-full bg-amber-400 hover:bg-amber-500 disabled:bg-yellow-200 disabled:text-yellow-600 text-yellow-950 font-bold py-4 rounded-xl shadow-lg transition-all flex items-center justify-center space-x-2 group mt-6"
            >
              {isAuthLoading ? (
                <Loader2 size={20} className="animate-spin" />
              ) : (
                <>
                  <span>{isLoginView ? t('auth') : t('reg')}</span>
                  <ArrowRight size={20} className="group-hover:translate-x-1 transition-transform" />
                </>
              )}
            </button>
          </form>
          
          <button 
            onClick={() => { setIsLoginView(!isLoginView); setAuthError(''); }} 
            className="w-full text-center mt-6 text-sm text-yellow-600 hover:text-amber-600 transition-colors font-medium"
          >
            {isLoginView 
              ? (accountData ? t('resetAcc') : t('needAcc')) 
              : t('hasAcc')}
          </button>
        </div>
      </div>
    );
  }

  // --- MAIN APP UI ---
  return (
    <div className="min-h-screen bg-yellow-50 text-yellow-950 font-sans flex h-screen overflow-hidden">
      {isSidebarOpen && <div className="fixed inset-0 bg-yellow-950/20 backdrop-blur-sm z-20 md:hidden" onClick={() => setIsSidebarOpen(false)} />}
      <aside className={`fixed md:relative z-30 h-full bg-yellow-100/50 transition-all duration-300 flex flex-col shrink-0 overflow-hidden ${isSidebarOpen ? 'w-72 border-r border-yellow-200' : 'w-0'}`}>
        <div className="w-72 flex flex-col h-full">
          <div className="p-4 border-b border-yellow-200 flex items-center justify-between">
            <div className="flex items-center space-x-2">
              <div className="bg-amber-400 p-1.5 rounded-lg text-yellow-950"><LemonIcon size={20} /></div>
              <h1 className="text-xl font-bold tracking-tight text-yellow-900">LEMUN</h1>
            </div>
            <button onClick={() => setIsSidebarOpen(false)} className="p-1.5 text-yellow-600 hover:bg-yellow-200 rounded-md"><X size={20} /></button>
          </div>
          <div className="p-4"><button onClick={handleNewChat} className="w-full flex items-center justify-center space-x-2 bg-white/80 hover:bg-white text-yellow-800 border border-yellow-200 py-2.5 rounded-xl transition-all font-medium"><Plus size={18} /><span>{t('newChat')}</span></button></div>
          <div className="flex-1 overflow-y-auto px-3 pb-4 space-y-1">
            <p className="px-3 text-[10px] font-bold text-yellow-600/70 uppercase tracking-widest mb-2 mt-4">{t('history')}</p>
            {chats.map(chat => (
              <button key={chat.id} onClick={() => switchChat(chat.id)} className={`w-full flex items-center space-x-3 px-3 py-2.5 rounded-lg text-left transition-all ${activeChatId === chat.id ? 'bg-amber-200/50 text-amber-950 font-medium' : 'text-yellow-700 hover:bg-yellow-200/50'}`}>
                <MessageSquare size={16} className={activeChatId === chat.id ? 'text-amber-600' : 'text-yellow-600/70'} /><span className="truncate text-sm">{chat.title}</span>
              </button>
            ))}
          </div>
          
          <div className="p-4 border-t border-yellow-200 bg-yellow-100 space-y-1">
            <div className="mb-2 px-3 py-2 bg-white/60 rounded-lg flex items-center space-x-3 border border-yellow-200/50">
               <div className="bg-amber-300 text-amber-950 rounded-full w-8 h-8 flex items-center justify-center font-bold text-sm uppercase">
                 {accountData?.name ? accountData.name.charAt(0) : 'U'}
               </div>
               <div className="overflow-hidden">
                 <p className="text-xs font-bold text-yellow-900 truncate">{accountData?.name || 'User'}</p>
                 <p className="text-[10px] text-yellow-600 truncate">{accountData?.email || t('loggedIn')}</p>
               </div>
            </div>

            <button onClick={() => {
              setTempPrompt(systemPrompt);
              setTempTtsVoice(ttsVoice);
              setTempAiLanguage(aiLanguage);
              setIsSettingsOpen(true);
            }} className="w-full flex items-center space-x-3 px-3 py-2.5 rounded-lg text-yellow-700 hover:bg-yellow-200/50 font-medium transition-all text-sm"><Settings size={18} /><span>{t('settings')}</span></button>
            <button onClick={handleLogOut} className="w-full flex items-center space-x-3 px-3 py-2.5 rounded-lg text-red-600 hover:bg-red-50 font-medium transition-all text-sm"><Lock size={18} /><span>{t('logout')}</span></button>
          </div>
        </div>
      </aside>

      <main className="flex-1 flex flex-col h-full bg-yellow-50 relative min-w-0">
        <header className="bg-yellow-50/90 backdrop-blur-md border-b border-yellow-200 p-4 flex items-center justify-between z-10">
          <div className="flex items-center">
            {!isSidebarOpen && <button onClick={() => setIsSidebarOpen(true)} className="p-2 mr-3 text-yellow-600 border border-yellow-200 rounded-lg hover:bg-yellow-100"><Menu size={20} /></button>}
            <div>
              <h2 className="text-lg font-bold truncate md:max-w-md text-yellow-950">{activeChat.title}</h2>
              <div className="flex items-center space-x-3 mt-1">
                <p className="text-xs text-amber-600 font-medium flex items-center"><Sparkles size={12} className="mr-1 animate-pulse" />{t('synced')}</p>
                <p className="text-[10px] text-yellow-600/80 font-bold uppercase tracking-wider flex items-center"><Globe size={10} className="mr-1 text-yellow-500" />{aiLanguage}</p>
              </div>
            </div>
          </div>
          <div className="flex items-center space-x-2">
            <div className="relative">
              <button onClick={() => setIsModeMenuOpen(!isModeMenuOpen)} className={`flex items-center space-x-1.5 text-xs font-bold px-3 py-1.5 rounded-full border shadow-sm transition-all ${activeMode === 'little' ? 'bg-green-100 text-green-800 border-green-300' : activeMode === 'big' ? 'bg-blue-100 text-blue-800 border-blue-300' : 'bg-red-100 text-red-800 border-red-300'}`}>
                {activeMode === 'little' ? <Zap size={14} /> : activeMode === 'big' ? <Brain size={14} /> : <Flame size={14} />}
                <span className="hidden sm:inline uppercase tracking-tight">{t(activeMode)}</span><ChevronDown size={14} className={isModeMenuOpen ? 'rotate-180' : ''} />
              </button>
              {isModeMenuOpen && <div className="absolute right-0 mt-2 w-48 bg-white border border-yellow-200 rounded-xl shadow-xl z-50 p-1 animate-in fade-in slide-in-from-top-2">
                {['little', 'big', 'spicy'].map(m => (
                  <button key={m} onClick={() => { setActiveMode(m); setIsModeMenuOpen(false); }} className={`w-full text-left px-3 py-2 rounded-lg text-sm font-medium transition-colors ${activeMode === m ? 'bg-yellow-100 text-yellow-950' : 'hover:bg-yellow-50 text-yellow-700'}`}>{t(m)}</button>
                ))}
              </div>}
            </div>
          </div>
        </header>

        <div className="flex-1 overflow-y-auto p-4 sm:p-6 space-y-6 bg-yellow-50/60">
          {activeChat.messages.map((msg, i) => (
            <div key={i} className={`flex ${msg.role === 'user' ? 'justify-end' : 'justify-start'} animate-in fade-in slide-in-from-bottom-2`}>
              <div className={`flex max-w-[90%] sm:max-w-[80%] ${msg.role === 'user' ? 'flex-row-reverse space-x-reverse' : 'flex-row'} items-start space-x-3`}>
                <div className={`shrink-0 w-8 h-8 rounded-full flex items-center justify-center shadow-sm ${msg.role === 'user' ? 'bg-amber-400 text-yellow-950' : 'bg-white text-amber-500 border border-yellow-200'}`}>{msg.role === 'user' ? <User size={16} /> : <LemonIcon size={18} />}</div>
                <div className={`p-4 rounded-2xl shadow-sm leading-relaxed ${msg.role === 'user' ? 'bg-amber-400 text-yellow-950 rounded-tr-sm' : 'bg-white text-yellow-950 border border-yellow-200 rounded-tl-sm'}`}>
                  <MessageContent text={msg.text} t={t} />
                  
                  {msg.role === 'model' && (
                    <div className="mt-3 pt-2 border-t border-yellow-100/50 flex justify-end">
                      <button
                        onClick={() => handleTTS(msg.text, i)}
                        disabled={isTTSLoading !== null && isTTSLoading !== i}
                        className="flex items-center space-x-1 px-2.5 py-1.5 bg-yellow-50 hover:bg-yellow-100 text-yellow-700 rounded-lg text-xs font-medium transition-colors border border-yellow-200/60 disabled:opacity-50"
                      >
                        {isTTSLoading === i ? <Loader2 size={14} className="animate-spin" /> : (playingIndex === i ? <Square size={14} className="text-red-500" /> : <Volume2 size={14} />)}
                        <span>{isTTSLoading === i ? t('loading') : (playingIndex === i ? t('stop') : t('read'))}</span>
                      </button>
                    </div>
                  )}

                  {msg.image && msg.image.startsWith('data:image') && <img src={msg.image} className="mt-4 rounded-xl border border-yellow-100 max-w-full shadow-sm" alt="AI Generated" />}
                  {msg.image === "[IMAGE_PLACEHOLDER]" && <div className="mt-3 p-3 bg-yellow-50 rounded-lg text-xs text-yellow-600 border border-dashed border-yellow-300 flex items-center space-x-2"><ImageIcon size={14} /><span>{t('imgCleared')}</span></div>}
                </div>
              </div>
            </div>
          ))}
          {isLoading && (
            <div className="flex justify-start animate-in fade-in"><div className="flex items-start space-x-3">
              <div className="shrink-0 w-8 h-8 rounded-full bg-white text-amber-500 border border-yellow-200 flex items-center justify-center shadow-sm"><LemonIcon size={18} /></div>
              <div className="bg-white border border-yellow-200 p-4 rounded-2xl rounded-tl-sm flex items-center space-x-2 text-yellow-600 shadow-sm"><Loader2 size={16} className="animate-spin text-amber-500" /><span className="text-sm font-medium animate-pulse">{loadingText}</span></div>
            </div></div>
          )}
          {error && <div className="text-center p-3 bg-red-50 border border-red-200 rounded-xl text-red-600 text-sm font-medium">{error}</div>}
          <div ref={messagesEndRef} />
        </div>

        <div className="p-4 sm:p-6 bg-yellow-50 border-t border-yellow-200">
          <form onSubmit={handleSendMessage} className="relative flex items-center max-w-5xl mx-auto group">
            <input type="text" value={input} onChange={(e) => setInput(e.target.value)} placeholder={t('ask')} disabled={isLoading} className="w-full bg-white border border-yellow-300 focus:border-amber-400 focus:ring-4 focus:ring-amber-400/10 rounded-2xl py-4 pl-5 pr-14 text-yellow-950 placeholder-yellow-500 outline-none transition-all disabled:opacity-50 shadow-sm" />
            <button type="submit" disabled={!input.trim() || isLoading} className="absolute right-2.5 p-2.5 bg-amber-400 hover:bg-amber-500 disabled:bg-yellow-200 disabled:text-yellow-500 text-yellow-950 rounded-xl transition-all shadow-sm focus:outline-none"><Send size={20} className={input.trim() && !isLoading ? 'translate-x-0.5 -translate-y-0.5' : ''} /></button>
          </form>
          <div className="text-center mt-3 text-[10px] text-yellow-600/70 font-bold uppercase tracking-widest">{t('footer')}</div>
        </div>
      </main>

      {isSettingsOpen && <div className="fixed inset-0 bg-yellow-950/40 backdrop-blur-sm z-50 flex items-center justify-center p-4">
        <div className="bg-white rounded-3xl shadow-2xl w-full max-w-lg overflow-hidden animate-in zoom-in-95 duration-200 border border-yellow-200">
          <div className="p-6 border-b border-yellow-100 flex justify-between items-center bg-yellow-50">
            <div className="flex items-center space-x-2 text-yellow-950"><Settings size={20} className="text-amber-500" /><h2 className="text-lg font-bold">{t('settings')}</h2></div>
            <button onClick={() => setIsSettingsOpen(false)} className="text-yellow-600 hover:bg-yellow-200 p-2 rounded-xl transition-all"><X size={20} /></button>
          </div>
          <div className="p-6 space-y-6 overflow-y-auto max-h-[60vh]">
            <div className="grid grid-cols-2 gap-4">
              <CustomSelect 
                label={t('lang')}
                icon={Globe}
                value={tempAiLanguage}
                onChange={setTempAiLanguage}
                options={[
                  { value: 'English', label: 'English' },
                  { value: 'Spanish', label: 'Español (Spanish)' },
                  { value: 'French', label: 'Français (French)' },
                  { value: 'German', label: 'Deutsch (German)' },
                  { value: 'Italian', label: 'Italiano (Italian)' },
                  { value: 'Portuguese', label: 'Português (Portuguese)' },
                  { value: 'Japanese', label: '日本語 (Japanese)' },
                  { value: 'Korean', label: '한국어 (Korean)' },
                  { value: 'Arabic', label: 'العربية (Arabic)' }
                ]}
              />
              
              <CustomSelect 
                label={t('voice')}
                icon={Volume2}
                value={tempTtsVoice}
                onChange={setTempTtsVoice}
                options={[
                  { value: 'Kore', label: 'Kore (Female)' },
                  { value: 'Charon', label: 'Charon (Male)' },
                  { value: 'Aoede', label: 'Aoede (Female)' },
                  { value: 'Fenrir', label: 'Fenrir (Male)' },
                  { value: 'Puck', label: 'Puck (Male)' },
                  { value: 'Zephyr', label: 'Zephyr (Female)' }
                ]}
              />
            </div>
            
            <div className="space-y-2">
              <label className="block text-xs font-bold text-yellow-600 uppercase tracking-widest">{t('base')}</label>
              <textarea value={tempPrompt} onChange={(e) => setTempPrompt(e.target.value)} className="w-full h-32 p-4 bg-yellow-50 border border-yellow-200 rounded-2xl text-sm text-yellow-950 focus:ring-4 focus:ring-amber-400/20 focus:border-amber-400 outline-none transition-all resize-none" />
            </div>
          </div>
          <div className="p-4 border-t border-yellow-100 bg-yellow-50 flex justify-end space-x-3">
            <button onClick={() => setIsSettingsOpen(false)} className="px-5 py-2.5 text-sm font-bold text-yellow-700 hover:text-yellow-900 transition-colors">{t('cancel')}</button>
            <button onClick={() => { 
              setSystemPrompt(tempPrompt); 
              setTtsVoice(tempTtsVoice);
              setAiLanguage(tempAiLanguage);
              setIsSettingsOpen(false); 
              
              if (firebaseUser) {
                const profileRef = doc(db, 'artifacts', appId, 'users', firebaseUser.uid, 'account', 'profile');
                setDoc(profileRef, {
                  settings: { voice: tempTtsVoice, language: tempAiLanguage, prompt: tempPrompt }
                }, { merge: true });
              }
            }} className="px-6 py-2.5 bg-amber-400 text-yellow-950 font-bold rounded-xl shadow-lg hover:bg-amber-500 transition-all">{t('save')}</button>
          </div>
        </div>
      </div>}
    </div>
  );
}