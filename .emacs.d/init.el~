;;; myeditor --- remover boas vindas:
;;; lipar o emacs:
(setq inhibit-startup-message t)

;; remover Menus
(tool-bar-mode -1)
(menu-bar-mode -1)

;;remover barra de rolagem
(scroll-bar-mode -1)

;; Numeros de nas linhas

(global-linum-mode t)

;;Tamanho da fonte
(set-face-attribute 'default nil :height 150)


;; pacotes
(require 'package)
(setq packge-enable-at-startup nil); diligar o gereciade de pacote nativo

; MELPA -REPOSITORIO

(add-to-list 'package-archives
             '("melpa-stable" . "https://stable.melpa.org/packages/") t)


(package-initialize);inicializador de pacote
(unless (package-installed-p 'use-package)
  (package-refresh-contents)
  (package-install 'use-package)
)


(use-package try
    :ensure t)
(use-package which-key
  :ensure t
  :config
    (progn
      (which-key-setup-side-window-right-bottom)
      (which-key-mode)
    )
    )
(use-package auto-complete
  :ensure t
  :init
  (progn
    (ac-config-default)
    (global-auto-complete-mode t)
    )
  )

(use-package all-the-icons
  :ensure t
  :if (display-graphic-p))


(use-package neotree
  :ensure t
  :bind (("C-\\" . 'neotree-toggle))
  )
(use-package ace-window
  :ensure t
  :bind (("C-x o" . ace-window)))
(use-package ergoemacs-mode
  :ensure t
  :config
  (progn
    (setq ergoemacs-theme nil)
    (setq ergoemacs-keyborad-layout "us")
    (ergoemacs-mode 1)))


;; thema
(use-package rebecca-theme
  :ensure t
  :config (load-theme 'rebecca))

(use-package flycheck
  :ensure t
  :init (global-flycheck-mode t))


(use-package markdown-mode
  :ensure t
  :mode ("README\\.md\\'" . gfm-mode)
  :init (setq markdown-command "multimarkdown"))

;; Atalhos
(global-set-key (kbd "C-<tab>") 'other-window)
;; Controle de janelas
(global-set-key (kbd "M-<down>") 'enlarge-window)
(global-set-key (kbd "M-<up>") 'shrink-window)
(global-set-key (kbd "M-<left>") 'enlarge-window-horizontally)
(global-set-key (kbd "M-<right>") 'shrink-window-horizontally)


;; MELPA config
(custom-set-variables
 ;; custom-set-variables was added by Custom.
 ;; If you edit it by hand, you could mess it up, so be careful.
 ;; Your init file should contain only one such instance.
 ;; If there is more than one, they won't work right.
 '(custom-safe-themes
   '("7178dc309d5bb89e9de6feddd71058ddf8cb947bbf08ea6c7799a03ae690449e" default))
 '(package-selected-packages
   '(markdown-mode flycheck rebecca-theme ergoemacs-mode ace-window auto-complete use-package)))
(custom-set-faces
 ;; custom-set-faces was added by Custom.
 ;; If you edit it by hand, you could mess it up, so be careful.
 ;; Your init file should contain only one such instance.
 ;; If there is more than one, they won't work right.
 )
