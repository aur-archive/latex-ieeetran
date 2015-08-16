#Maintainer: Egon Geerardyn < egon dot geerardyn at gmail dot com >
#Contributor: Samsagax <samsagax at gmail dot com>

pkgname=latex-ieeetran
pkgver=1.8a
pkgrel=3
pkgdesc="Official LaTeX class for IEEE transaction and conference papers"
arch=('any')
url="http://www.ctan.org/tex-archive/macros/latex/contrib/IEEEtran/"
license=('LPPL')
groups=()
depends=('texlive-bin')
makedepends=('tar' 'gzip')
optdepends=('xpdf: for viewing the manual')
backup=()
options=()
install=texlive.install
source=(
'http://mirror.ctan.org/macros/latex/contrib/IEEEtran.zip'
'IEEEtranN.bst.patch'
)
md5sums=(
'1cdd148fce607cdab729d41cb97fa4a4'
'd7d782750ebf4e9aaaef6e88170f5e8b'
)

package() {
  install -d ${pkgdir}/usr/share/texmf-dist/tex/latex/
  cp -r ${srcdir}/IEEEtran ${pkgdir}/usr/share/texmf-dist/tex/latex/
  install -d ${pkgdir}/usr/share/texmf-dist/bibtex/bst/IEEEtran/
  install -d ${pkgdir}/usr/share/texmf-dist/bibtex/bib/IEEEtran/
  # create a german version
  install ${srcdir}/IEEEtran/bibtex/IEEEtranN.bst ${pkgdir}/usr/share/texmf-dist/bibtex/bst/IEEEtran/IEEEtranN_DE.bst
  patch ${pkgdir}/usr/share/texmf-dist/bibtex/bst/IEEEtran/IEEEtranN_DE.bst IEEEtranN.bst.patch
  #copy original files
  install ${srcdir}/IEEEtran/bibtex/*.bst ${pkgdir}/usr/share/texmf-dist/bibtex/bst/IEEEtran/
  install ${srcdir}/IEEEtran/bibtex/*.bib ${pkgdir}/usr/share/texmf-dist/bibtex/bib/IEEEtran/
}

# vim:set ts=2 sw=2 et:
