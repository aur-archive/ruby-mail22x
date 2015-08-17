# Contributor: Emiliano Vavassori <syntaxerrormmm@gmail.com>
# Maintainer: Alexsandr Pavlov <kidoz at mail dot ru>
pkgname=ruby-mail22x
gemname=mail
pkgver=2.2.19
pkgrel=2
pkgdesc="Handle emails generation, parsing and sending in a simple, rubyesque manner"
arch=('any')
url="http://github.com/mikel/mail"
license=('MIT')
depends=('ruby' 'ruby-i18n>=0.4.0' 'ruby-treetop>=1.4.8' 'ruby-mime-types>=1.16' 'ruby-activesupport>=2.3.6')
makedepends=('rubygems')
source=(http://rubygems.org/downloads/${gemname}-${pkgver}.gem)
noextract=(${gemname}-${pkgver}.gem)
md5sums=('cc75d08765e10eec3adfa7d5a790dec3')

build() {
  cd "${srcdir}"
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  
  gem install --no-user-install --ignore-dependencies -i "${pkgdir}${_gemdir}" ${gemname}-${pkgver}.gem
}
