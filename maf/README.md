find ../ -name "*10yrs.db" -not -path "*technical/*" | xargs -I'{}' ln -s {} .

find ../ -name "*10yrs.db" | xargs -I'{}' ln -s {} .

