# Pre-built image published by GitHub Actions to GHCR.
# __GHCR_IMAGE__ is substituted during deploy.
FROM __GHCR_IMAGE__

ENV PORT=7860
ENV BIND_HOST=0.0.0.0
ENV NODE_ENV=production

EXPOSE 7860

ENTRYPOINT ["node", "dist/server/index.js"]
CMD []
