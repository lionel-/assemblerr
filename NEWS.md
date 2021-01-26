# assemblerr (development version)
* prediction declarations for observations do not longer need a left-hand side, i.e., `obs_additive(~C["central"])` is now valid.
* `pk_elimination_mm` has been replaced with `pk_elimination_nl` to clarify that the default parameterization is not the classical MM model. Additionally, `pk_elimination_nl` allows selecting the classical parameterization using `pk_elimination_nl(prm_vmax = prm_log_normal("vmax"), prm_clmm = NULL)`
* unsupported building blocks are now ignored with a warning when added to a model (e.g., `pk_model()+compartment('central')`) 
* option to include estimation & covariance step records in generated NONMEM model through `render(m, options = assemblerr_options(default_record.covariance_step = nm_covariance()))`
* Added a `NEWS.md` file to track changes to the package.