#
# Copyright (c) 2018 Enrico M. Crisostomo
#
# This program is free software; you can redistribute it and/or modify it under
# the terms of the GNU General Public License as published by the Free Software
# Foundation; either version 3, or (at your option) any later version.
#
# This program is distributed in the hope that it will be useful, but WITHOUT
# ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
# FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more
# details.
#
# You should have received a copy of the GNU General Public License along with
# this program.  If not, see <http://www.gnu.org/licenses/>.
#
ACLOCAL_AMFLAGS = -I m4

dist_doc_DATA  = README.md README.gnu-build-system
dist_doc_DATA += AUTHORS CONTRIBUTING.md COPYING LICENSE NEWS

bin_SCRIPTS  = scripts/port-gen
CLEANFILES   = $(bin_SCRIPTS)

nobase_dist_pkgdata_DATA = templates/github.in

edit = sed \
	-e 's|@bindir\[@\]|$(bindir)|g' \
	-e 's|@pkgdatadir\[@\]|$(pkgdatadir)|g' \
	-e 's|@prefix\[@\]|$(prefix)|g'

scripts/port-gen: Makefile
	rm -f $@ $@.tmp
	$(edit) $@.in >$@.tmp
	mv $@.tmp $@

scripts/port-gen: scripts/port-gen.in

dist-hook:
# The recipe cannot assume a file in $(distdir) is writable.
	chmod u+w $(distdir)/ChangeLog
	git log --oneline --decorate >> $(distdir)/ChangeLog
