import React, { useState } from "react";
import { Button } from "/components/ui/button";
import { Card, CardContent, CardDescription, CardHeader, CardTitle } from "/components/ui/card";
import { Input } from "/components/ui/input";
import { Textarea } from "/components/ui/textarea";
import { Label } from "/components/ui/label";

const VideoEditingWebsite = () => {
  const [name, setName] = useState("");
  const [email, setEmail] = useState("");
  const [message, setMessage] = useState("");

  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    // Simulação de envio do formulário
    console.log({ name, email, message });
    alert("Mensagem enviada! Entraremos em contato em breve.");
    setName("");
    setEmail("");
    setMessage("");
  };

  return (
    <div className="min-h-screen bg-background text-foreground">
      {/* Header */}
      <header className="fixed top-0 w-full bg-background/95 backdrop-blur supports-[backdrop-filter]:bg-background/60 z-50 border-b border-border">
        <div className="container mx-auto px-4 py-4 flex justify-between items-center">
          <div className="flex items-center space-x-2">
            <div className="w-8 h-8 bg-primary rounded-full flex items-center justify-center">
              <span className="text-white font-bold text-lg">V</span>
            </div>
            <span className="font-bold text-xl">VideoCraft</span>
          </div>
          <nav className="hidden md:flex space-x-8">
            <a href="#servicos" className="hover:text-primary transition-colors">Serviços</a>
            <a href="#portfolio" className="hover:text-primary transition-colors">Portfólio</a>
            <a href="#depoimentos" className="hover:text-primary transition-colors">Depoimentos</a>
            <a href="#contato" className="hover:text-primary transition-colors">Contato</a>
          </nav>
          <Button className="md:hidden">Menu</Button>
        </div>
      </header>

      {/* Hero Section */}
      <section className="pt-32 pb-20 px-4 text-center">
        <div className="container mx-auto max-w-4xl">
          <h1 className="text-4xl md:text-6xl font-bold mb-6">
            Transforme suas ideias em <span className="text-primary">vídeos incríveis</span>
          </h1>
          <p className="text-xl text-muted-foreground mb-8 max-w-2xl mx-auto">
            Edição profissional de vídeo para YouTube, redes sociais, eventos e muito mais. 
            Destaque seu conteúdo com qualidade cinematográfica.
          </p>
          <div className="flex flex-col sm:flex-row gap-4 justify-center">
            <Button size="lg" className="bg-primary hover:bg-primary/90">
              Solicitar Orçamento
            </Button>
            <Button variant="outline" size="lg">
              Ver Portfólio
            </Button>
          </div>
        </div>
      </section>

      {/* Serviços */}
      <section id="servicos" className="py-20 bg-muted/50">
        <div className="container mx-auto px-4">
          <h2 className="text-3xl font-bold text-center mb-12">Nossos Serviços</h2>
          <div className="grid md:grid-cols-3 gap-8">
            <Card>
              <CardHeader>
                <CardTitle>Edição para YouTube</CardTitle>
                <CardDescription>Vídeos otimizados para engajamento</CardDescription>
              </CardHeader>
              <CardContent>
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x250?prompt=Professional YouTube video editing setup with multiple screens, editing software interface, and colorful thumbnails&id=servico1" 
                  alt="Setup profissional de edição para YouTube com múltiplas telas e interface de software" 
                  className="w-full h-48 object-cover rounded-lg mb-4"
                />
                <p>Corte preciso, transições suaves, correção de cor, legendas e thumbnails atraentes.</p>
                <ul className="mt-4 space-y-2">
                  <li>• Edição multicam</li>
                  <li>• Motion graphics</li>
                  <li>• Otimização para SEO</li>
                </ul>
              </CardContent>
            </Card>

            <Card>
              <CardHeader>
                <CardTitle>Redes Sociais</CardTitle>
                <CardDescription>Conteúdo viral para todas as plataformas</CardDescription>
              </CardHeader>
              <CardContent>
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x250?prompt=Social media content creation with smartphone showing Instagram Reels, TikTok videos, and engaging short-form content&id=servico2" 
                  alt="Criação de conteúdo para redes sociais mostrando Reels, TikTok e conteúdo short-form" 
                  className="w-full h-48 object-cover rounded-lg mb-4"
                />
                <p>Vídeos curtos e impactantes para Instagram, TikTok, Facebook e Twitter.</p>
                <ul className="mt-4 space-y-2">
                  <li>• Formatos verticais</li>
                  <li>• Legendas automáticas</li>
                  <li>• Edição rápida</li>
                </ul>
              </CardContent>
            </Card>

            <Card>
              <CardHeader>
                <CardTitle>Eventos e Casamentos</CardTitle>
                <CardDescription>Memórias que duram para sempre</CardDescription>
              </CardHeader>
              <CardContent>
                <img 
                  src="https://placeholder-image-service.onrender.com/image/400x250?prompt=Wedding video editing with romantic scenes, drone footage, and elegant transitions&id=servico3" 
                  alt="Edição de vídeo de casamento com cenas românticas, footage de drone e transições elegantes" 
                  className="w-full h-48 object-cover rounded-lg mb-4"
                />
                <p>Captura e edição profissional para casamentos, eventos corporativos e festas.</p>
                <ul className="mt-4 space-y-2">
                  <li>• Edição emocional</li>
                  <li>• Footage de drone</li>
                  <li>• Entrega rápida</li>
                </ul>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      {/* Portfólio */}
      <section id="portfolio" className="py-20">
        <div className="container mx-auto px-4">
          <h2 className="text-3xl font-bold text-center mb-12">Nosso Portfólio</h2>
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            {/* Projeto 1 */}
            <div className="group relative overflow-hidden rounded-lg">
              <img 
                src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Travel vlog video with beautiful landscapes, smooth transitions, and cinematic color grading&id=portfolio1" 
                alt="Vlog de viagem com paisagens deslumbrantes, transições suaves e correção de cor cinematográfica" 
                className="w-full h-64 object-cover transition-transform group-hover:scale-110"
              />
              <div className="absolute inset-0 bg-black/70 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                <div className="text-center text-white p-4">
                  <h3 className="font-bold text-lg">Vlog de Viagem</h3>
                  <p>Cinematografia premium</p>
                </div>
              </div>
            </div>

            {/* Projeto 2 */}
            <div className="group relative overflow-hidden rounded-lg">
              <img 
                src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Corporate training video with professional presentation, graphics, and clear explanations&id=portfolio2" 
                alt="Vídeo corporativo de treinamento com apresentação profissional, gráficos e explicações claras" 
                className="w-full h-64 object-cover transition-transform group-hover:scale-110"
              />
              <div className="absolute inset-0 bg-black/70 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                <div className="text-center text-white p-4">
                  <h3 className="font-bold text-lg">Treinamento Corporativo</h3>
                  <p>Conteúdo educativo</p>
                </div>
              </div>
            </div>

            {/* Projeto 3 */}
            <div className="group relative overflow-hidden rounded-lg">
              <img 
                src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Music video with artistic editing, rhythmic cuts, and creative visual effects&id=portfolio3" 
                alt="Videoclipe musical com edição artística, cortes rítmicos e efeitos visuais criativos" 
                className="w-full h-64 object-cover transition-transform group-hover:scale-110"
              />
              <div className="absolute inset-0 bg-black/70 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                <div className="text-center text-white p-4">
                  <h3 className="font-bold text-lg">Videoclipe Musical</h3>
                  <p>Edição criativa</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Depoimentos */}
      <section id="depoimentos" className="py-20 bg-muted/50">
        <div className="container mx-auto px-4">
          <h2 className="text-3xl font-bold text-center mb-12">O que nossos clientes dizem</h2>
          <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
            <Card>
              <CardContent className="pt-6">
                <div className="flex items-center mb-4">
                  <div className="w-12 h-12 bg-primary/10 rounded-full flex items-center justify-center">
                    <span className="text-primary font-bold">M</span>
                  </div>
                  <div className="ml-4">
                    <h4 className="font-semibold">Maria Silva</h4>
                    <p className="text-sm text-muted-foreground">YouTuber</p>
                  </div>
                </div>
                <p className="text-muted-foreground">
                  "Incrível! Meus vídeos nunca tiveram tanto engajamento. A edição transformou completamente meu canal."
                </p>
              </CardContent>
            </Card>

            <Card>
              <CardContent className="pt-6">
                <div className="flex items-center mb-4">
                  <div className="w-12 h-12 bg-primary/10 rounded-full flex items-center justify-center">
                    <span className="text-primary font-bold">J</span>
                  </div>
                  <div className="ml-4">
                    <h4 className="font-semibold">João Santos</h4>
                    <p className="text-sm text-muted-foreground">Empresário</p>
                  </div>
                </div>
                <p className="text-muted-foreground">
                  "Profissionalismo total! Entregaram nosso vídeo corporativo antes do prazo e com qualidade excepcional."
                </p>
              </CardContent>
            </Card>

            <Card>
              <CardContent className="pt-6">
                <div className="flex items-center mb-4">
                  <div className="w-12 h-12 bg-primary/10 rounded-full flex items-center justify-center">
                    <span className="text-primary font-bold">A</span>
                  </div>
                  <div className="ml-4">
                    <h4 className="font-semibold">Ana Costa</h4>
                    <p className="text-sm text-muted-foreground">Noiva</p>
                  </div>
                </div>
                <p className="text-muted-foreground">
                  "O vídeo do nosso casamento ficou perfeito! Capturaram cada momento especial de maneira tão emocionante."
                </p>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      {/* Contato */}
      <section id="contato" className="py-20">
        <div className="container mx-auto px-4 max-w-4xl">
          <h2 className="text-3xl font-bold text-center mb-12">Entre em Contato</h2>
          <div className="grid md:grid-cols-2 gap-12">
            <div>
              <h3 className="text-xl font-semibold mb-4">Vamos conversar sobre seu projeto</h3>
              <p className="text-muted-foreground mb-6">
                Entre em contato para discutir suas necessidades de edição de vídeo. 
                Respondemos em até 24 horas.
              </p>
              <div className="space-y-4">
                <div className="flex items-center">
                  <div className="w-8 h-8 bg-primary/10 rounded-full flex items-center justify-center mr-3">
                    <span className="text-primary">✉️</span>
                  </div>
                  <span>contato@videocraft.com</span>
                </div>
                <div className="flex items-center">
                  <div className="w-8 h-8 bg-primary/10 rounded-full flex items-center justify-center mr-3">
                    <span className="text-primary">📞</span>
                  </div>
                  <span>+55 (11) 99999-9999</span>
                </div>
              </div>
            </div>

            <form onSubmit={handleSubmit} className="space-y-4">
              <div>
                <Label htmlFor="name">Nome</Label>
                <Input
                  id="name"
                  value={name}
                  onChange={(e) => setName(e.target.value)}
                  required
                />
              </div>
              <div>
                <Label htmlFor="email">Email</Label>
                <Input
                  id="email"
                  type="email"
                  value={email}
                  onChange={(e) => setEmail(e.target.value)}
                  required
                />
              </div>
              <div>
                <Label htmlFor="message">Mensagem</Label>
                <Textarea
                  id="message"
                  rows={4}
                  value={message}
                  onChange={(e) => setMessage(e.target.value)}
                  required
                />
              </div>
              <Button type="submit" className="w-full bg-primary hover:bg-primary/90">
                Enviar Mensagem
              </Button>
            </form>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-muted py-12 border-t border-border">
        <div className="container mx-auto px-4 text-center">
          <div className="flex justify-center mb-6">
            <div className="w-10 h-10 bg-primary rounded-full flex items-center justify-center">
              <span className="text-white font-bold">V</span>
            </div>
          </div>
          <p className="text-muted-foreground mb-4">
            Transformando ideias em vídeos extraordinários
          </p>
          <div className="flex justify-center space-x-6 mb-6">
            <a href="#" className="text-muted-foreground hover:text-primary">Instagram</a>
            <a href="#" className="text-muted-foreground hover:text-primary">YouTube</a>
            <a href="#" className="text-muted-foreground hover:text-primary">LinkedIn</a>
          </div>
          <p className="text-sm text-muted-foreground">
            © 2024 VideoCraft. Todos os direitos reservados.
          </p>
        </div>
      </footer>
    </div>
  );
};

export default VideoEditingWebsite;
