# HealthTechGov

HealthTechGov is a small project exploring how GitHub and AWS DevOps practices could improve project coordination, software delivery, and security in a healthcare setting. The repository currently contains documentation and a minimal Python demonstration; it is not a deployed healthcare service.

## Repository structure

- `src/` - Python source code.
- `docs/` - Project, workflow, and security/compliance guidance.
- `.gitignore` - Excludes local environments, generated files, and local secrets.

## Run the demo

Use Python 3 and run:

```powershell
python src/index.py
```

## Security and project status

Do not commit passwords, access keys, or real patient information. Use synthetic data for any development or testing. AWS deployment, CI/CD, IAM, and monitoring are planned work; the documentation in this repository is not evidence of a deployed system or compliance certification.
