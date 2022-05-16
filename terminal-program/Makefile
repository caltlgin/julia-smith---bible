juliasmith: juliasmith.sh juliasmith.awk juliasmith.tsv
	cat juliasmith.sh > $@

	echo 'exit 0' >> $@

	echo '#EOF' >> $@
	tar czf - juliasmith.awk juliasmith.tsv >> $@

	chmod +x $@

test: juliasmith.sh
	shellcheck -s sh juliasmith.sh

.PHONY: test
