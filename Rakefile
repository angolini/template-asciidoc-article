namespace :build do
  desc 'Generate HTML outputs'
  task :html do
    puts "Converting to HTML..."
    `bundle exec asciidoctor src/article.adoc -o article.html`
    puts " -- HTML output at article.html"
  end

  desc 'Generate PDF outputs'
  task :pdf do
    puts "Converting to PDF... (this one takes a while)"
    `bundle exec asciidoctor-pdf src/article.adoc -o article.pdf`
    puts " -- PDF  output at article.pdf"
  end
end

desc 'Build all default formats'
task :build => [ "build:html", "build:pdf" ]
