---
title: Comment... (Référence PIA Outlook 2013)
TOCTitle: How do I...
ms:assetid: ff647d52-bd32-4945-afa4-5b97d9a0d7dd
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612741(v=office.15)
ms:contentKeyID: 55119792
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bc4e19271e2747f5ffa8586b9f2ab226d6658b4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711720"
---
# <a name="how-do-i-outlook-2013-pia-reference"></a>Comment... (Référence PIA Outlook 2013)

Cette section contient des rubriques de tâches procédurales et des exemples de code en Visual Basic et en C\# qui montrent comment effectuer certaines tâches courantes dans Outlook.

Pour exécuter ces exemples de code, vous devez avoir installé Outlook 2010 et Visual Studio 2008 ou une version ultérieure de ces produits.

Les exemples de code dans cette section ne nécessitent pas que vous ayez installé les outils de développement Office pour Visual Studio. Toutefois, vous pouvez vous référer au portail [Prise en main du développement Office](https://developer.microsoft.com/office/docs) pour plus d’informations sur l’utilisation des outils et consulter [Solutions Outlook](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) pour certaines tâches procédurales de base écrites en code managé.

Les exemples de code de cette section vont des niveaux « débutant » à « intermédiaire », et certains d’entre eux sont adaptés de l’ouvrage [Programmation d’applications pour Microsoft Office Outlook 2007 (Programming Applications for Microsoft Office Outlook 2007)](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493).

L’équipe Documentation du développeur Office vous invite à communiquer vos idées et vos échantillons de code. Si nous utilisons vos exemples de code dans du contenu Outlook, nous identifierons votre travail à l’aide d’une signature et d’un lien vers votre site Web. Pour plus d’informations, veuillez nous contacter à docthis@microsoft.com.

## <a name="in-this-section"></a>Dans cette section 

[Comptes](accounts.md)

- [Obtenir des informations sur le compte](how-to-get-account-information.md)
- [Créer un élément à envoyer pour un compte spécifique basé sur le dossier actif](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md)
- [Obtenir le compte lié à un dossier](how-to-get-the-account-for-a-folder.md)
- [Obtenir des informations sur plusieurs comptes](how-to-get-information-about-multiple-accounts.md)
- [Envoyer un élément de courrier électronique à l’aide d’un compte Hotmail](how-to-send-a-mail-item-by-using-a-hotmail-account.md)

[Administration des compléments](add-in-administration.md)

- [Vérifier si Outlook est une application « Démarrer en un clic » sur un ordinateur](how-to-determine-whether-outlook-is-a-click-to-run-application-on-a-computer.md)


[Carnet d’adresses](address-book.md)

- [Afficher le carnet d’adresses correspondant à un dossier de Contacts dans la boîte de dialogue Sélectionner des noms](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)
- [Identifier la liste d’adresses globale ou un ensemble de listes d’adresses pour un magasin](how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store.md)
- [Énumérer les entrées de la liste d'adresses globale](how-to-enumerate-the-entries-in-the-global-address-list.md)
- [Afficher les listes d’adresses pour un profil](how-to-display-the-address-lists-for-a-profile.md)

[Rendez-vous](appointments.md)

- [Créer un événement sur toute la journée](how-to-create-an-appointment-that-is-an-all-day-event.md)
- [Créer un rendez-vous qui commence dans le fuseau horaire Pacifique et se termine dans le fuseau horaire Est](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)
- [Spécifier différents types de destinataires pour un élément de rendez-vous](how-to-specify-different-recipient-types-for-an-appointment-item.md)
- [Créer un rendez-vous périodique selon une périodicité par défaut.](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)
- [Créer un rendez-vous périodique ayant une périodicité hebdomadaire](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)
- [Créer un rendez-vous périodique annuel selon une périodicité de toutes les n années](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)
- [Trouver un rendez-vous spécifique dans une série de rendez-vous périodiques](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)
- [Créer une exception de rendez-vous dans une série de rendez-vous périodiques](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)
- [Créer un rappel pour un élément de rendez-vous](how-to-create-a-reminder-for-an-appointment-item.md)
- [Importer les données XML de rendez-vous dans les objets de rendez-vous Outlook](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)

[Pièces jointes](attachments.md)

- [Joindre un fichier à un élément de courrier](https://docs.microsoft.com/office/vba/outlook/How-to/Items-Folders-and-Stores/attach-a-file-to-a-mail-item)
- [Attacher un élément de Contact Outlook dans un message électronique](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/attach-an-outlook-contact-item-to-an-email-message)
- [Limiter la taille d'une pièce jointe à un message de courrier électronique Outlook](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/limit-the-size-of-an-attachment-to-an-outlook-email-message)
- [Modifier une pièce jointe d’un message électronique Outlook](https://docs.microsoft.com/office/vba/outlook/concepts/attachments/modify-an-attachment-of-an-outlook-email-message)
- [Supprimer par programme les pièces jointes de niveau 2 de sécurité contenues dans les messages et les enregistrer sur le disque](how-to-programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk.md)

[Calendrier](calendar.md)

- [Partager le planning de disponibilité pendant une période spécifiée dans un calendrier](how-to-share-free-busy-schedule-within-a-specified-period-in-a-calendar.md)
- [Partager des informations de calendrier par courrier électronique](how-to-share-calendar-information-through-e-mail.md)
- [Afficher le calendrier partagé d’un destinataire](how-to-display-a-shared-calendar-of-a-recipient.md)
- [Enregistrer un calendrier sur le disque](how-to-save-a-calendar-to-disk.md)
- [Ouvrir et afficher le contenu d’un fichier iCalendar](how-to-open-and-display-the-contents-of-an-icalendar-file.md)

[Catégories de couleurs](color-categories.md)

- [Énumérer et ajouter des catégories](how-to-enumerate-and-add-categories.md)
- [Affecter des catégories à un élément](how-to-assign-categories-to-an-item.md)

[Contacts](contacts.md)

- [Créer un élément de Contact](how-to-create-a-contact-item.md)
- [Créer un élément de Contact personnalisé](how-to-create-a-custom-contact-item.md)
- [Créer un élément de Contact à partir d’un fichier vCard et enregistrer l’élément dans un dossier](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)

[Conversations](conversations.md)

- [Obtenir et afficher les éléments dans une conversation](how-to-get-and-display-items-in-a-conversation.md)
- [Obtenir et énumérer les conversations sélectionnées](how-to-get-and-enumerate-selected-conversations.md)

[Cartes de visite électroniques](electronic-business-cards.md)

- [Modifier la mise en page d’une carte de visite électronique](how-to-modify-the-layout-of-an-electronic-business-card.md)
- [Envoyer un élément de courrier avec une carte de visite électronique](how-to-send-a-mail-item-with-an-electronic-business-card.md)

[Utilisateurs Exchange](exchange-users.md)

- [Informations sur l'utilisateur actuel](how-to-get-information-about-the-current-user.md)
- [Obtenir des informations sur toutes les listes de distribution dont l’utilisateur actuel est membre](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)
- [Créer une liste de distribution](how-to-create-a-distribution-list.md)
- [Obtenir les membres d’une liste de distribution Exchange](how-to-get-members-of-an-exchange-distribution-list.md)
- [Obtenir des informations sur le gestionnaire de l’utilisateur actuel](how-to-get-information-about-the-current-user-s-manager.md)
- [Obtenir des informations concernant la disponibilité d’un gestionnaire d’un utilisateur Exchange](how-to-get-availability-information-for-an-exchange-user-s-manager.md)
- [Vérifier la réponse d’un gestionnaire à une demande de réunion](how-to-check-a-manager-s-response-to-a-meeting-request.md)
- [Obtenir des informations sur les collaborateurs directs du gestionnaire de l’utilisateur actuel](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md)

[Dossiers](folders.md)

- [Ajouter un dossier à la liste des dossiers](how-to-add-a-folder-to-the-folder-list.md)
- [Énumérer les dossiers](how-to-enumerate-folders.md)
- [Obtenir un dossier par défaut et énumérer ses sous-dossiers](how-to-get-a-default-folder-and-enumerate-its-subfolders.md)
- [Obtenir un dossier à partir de son chemin d’accès](how-to-get-a-folder-based-on-its-folder-path.md)
- [Sélectionner un dossier et afficher les informations du dossier](how-to-select-a-folder-and-display-folder-information.md)
- [Obtenir la classe de message par défaut d’un dossier](how-to-get-the-default-message-class-of-a-folder.md)
- [Accéder aux données spécifiques à la solution stockées comme message masqué dans un dossier](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)
- [S’assurer que les propriétés des éléments personnalisés sont prises en charge dans les requêtes au niveau du dossier](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md)

[Éléments Outlook généraux](general-outlook-items.md)

- [Créer une classe d’assistance pour accéder aux membres d’un élément courant Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [Afficher les éléments sélectionnés dans l’Explorateur actif](how-to-display-selected-items-in-the-active-explorer.md)

[Partage de groupe](group-sharing.md)

- [S’abonner à un flux RSS](how-to-subscribe-to-an-rss-feed.md)
- [Synchroniser Outlook avec un dossier SharePoint](how-to-synchronize-outlook-with-a-sharepoint-folder.md)

[Courrier](mail.md)

- [Créer un élément de courrier à l’aide d’un modèle de message](how-to-create-a-mail-item-by-using-a-message-template.md)
- [Créer un élément de courrier, joindre un rapport et envoyer l’élément de courrier au gestionnaire de l’utilisateur](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md)
- [Envoyer un message électronique d’après l’adresse SMTP d’un compte](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md)
- [Ajouter des options de vote à un élément de courrier](how-to-add-voting-options-to-a-mail-item.md)
- [Ajouter une action personnalisée en guise de réponse à un élément de courrier](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md)
- [Obtenir l’adresse SMTP de l’expéditeur d’un élément de courrier](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md)
- [Spécifier différents types de destinataires pour un élément de courrier](how-to-specify-different-recipient-types-for-a-mail-item.md)

[Demandes de réunion](meeting-requests.md)

- [Créer une demande de réunion, ajouter des destinataires et spécifier un emplacement](how-to-create-a-meeting-request-add-recipients-and-specify-a-location.md)
- [Obtenir l’organisateur d’une réunion](how-to-get-the-organizer-of-a-meeting.md)
- [Consulter toutes les réponses à une demande de réunion](how-to-check-all-responses-to-a-meeting-request.md)
- [Rechercher l’élément de rendez-vous associé à une demande de réunion](how-to-find-the-appointment-item-associated-with-a-meeting-request.md)
- [Accepter automatiquement une demande de réunion](how-to-automatically-accept-a-meeting-request.md)
- [Inviter un utilisateur à répondre à une demande de réunion](how-to-prompt-a-user-to-respond-to-a-meeting-request.md)

[Destinataires](recipients.md)

- [Afficher la boîte de dialogue Sélectionner des noms pour résoudre des destinataires](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)
- [Utiliser la boîte de dialogue Sélectionner des noms pour obtenir et attribuer des destinataires à un rendez-vous](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)
- [Obtenir l'adresse de messagerie électronique d’un destinataire](how-to-get-the-e-mail-address-of-a-recipient.md)

[Règles](rules.md)

- [Créer une règle pour classer les éléments de courrier provenant d’un gestionnaire et les marquer pour assurer un suivi](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)
- [Exécuter une règle instantanément](how-to-execute-a-rule-instantly.md)
- [Exécuter une règle sur un ordinateur local](how-to-execute-a-rule-on-a-local-computer.md)
- [Créer une règle pour affecter des catégories aux éléments de courrier en fonction de plusieurs mots dans l’objet](how-to-create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject.md)


[Exemples de tâches utilisant des événements Outlook](sample-tasks-using-outlook-events.md)

- [Mettre en œuvre un wrapper pour les inspecteurs et suivre les événements au niveau des éléments dans chaque inspecteur](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)

[Rechercher et filtrer](search-and-filter.md)

- [Filtrer et énumérer efficacement les éléments d’un dossier](how-to-filter-and-efficiently-enumerate-items-in-a-folder.md)
- [Utiliser SetColumns pour énumérer efficacement les éléments d’un dossier](how-to-use-setcolumns-to-efficiently-enumerate-items-in-a-folder.md)
- [Utiliser les tableaux pour énumérer efficacement les éléments d’un dossier](how-to-use-arrays-to-efficiently-enumerate-items-in-a-folder.md)
- [Énumérer les éléments dans la Boîte de réception en fonction de l’heure de la dernière modification](how-to-enumerate-items-in-the-inbox-based-on-the-last-modification-time.md)
- [Filtrer et afficher les éléments de Boîte de réception modifiés le mois dernier](how-to-filter-and-display-inbox-items-modified-in-the-last-month.md)
- [Filtrer et afficher des propriétés à plusieurs valeurs lors de l’énumération d’éléments dans un dossier](how-to-filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder.md)
- [Filtrer et afficher des propriétés calculées lors de l’énumération d’éléments dans un dossier](how-to-filter-and-display-computed-properties-when-enumerating-items-in-a-folder.md)
- [Énumérer les éléments masqués d’un dossier](how-to-enumerate-hidden-items-in-a-folder.md)
- [Utiliser la recherche instantanée pour effectuer une recherche dans tous les dossiers et tous les magasins pour une expression dans l’objet](how-to-use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject.md)
- [Rechercher une expression dans le corps d’éléments d’un dossier](how-to-search-for-a-phrase-in-the-body-of-items-in-a-folder.md)
- [Rechercher les pièces jointes des éléments d’un dossier pour une expression exacte](how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase.md)
- [Effectuer des recherches et obtenir des rendez-vous dans un intervalle de temps](how-to-search-and-obtain-appointments-in-a-time-range.md)
- [Filtrer les rendez-vous périodiques et rechercher une chaîne dans l’objet](how-to-filter-recurring-appointments-and-search-for-a-string-in-the-subject.md)
- [Rechercher et obtenir des éléments dans une vue agrégée](how-to-search-and-obtain-items-in-an-aggregated-view.md)

[Sessions](sessions.md)

- [Obtenir et se connecter à une instance d’Outlook](how-to-get-and-log-on-to-an-instance-of-outlook.md)

[Magasins](stores.md)

- [Obtenir des informations sur les magasins dans un profil](how-to-get-information-about-stores-in-a-profile.md)
- [Ajouter ou supprimer un magasin](how-to-add-or-remove-a-store.md)

[Tâches](tasks.md)

- [Créer un élément de tâche](how-to-create-a-task-item.md)
- [Affecter une tâche à un destinataire](how-to-assign-a-task-to-a-recipient.md)
- [Afficher les éléments de demande de tâche envoyés à un destinataire](how-to-display-the-task-request-items-sent-to-a-recipient.md)
- [Répondre à un élément de demande de tâche](how-to-respond-to-a-task-request-item.md)
- [Créer une tâche périodique](how-to-create-a-recurring-task.md)
- [Marquer les éléments de courrier provenant d’un gestionnaire pour assurer un suivi](how-to-flag-mail-items-from-a-manager-for-follow-up.md)

[Affichages](views.md)

- [Créer un affichage](how-to-create-a-view.md)
- [Ajouter des champs à un affichage](how-to-add-fields-to-a-view.md)
- [Énumérer les éléments d’un affichage tableau](how-to-enumerate-items-in-a-table-view.md)



