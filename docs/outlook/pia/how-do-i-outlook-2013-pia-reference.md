---
title: Comment... (Référence PIA Outlook 2013)
TOCTitle: How do I...
ms:assetid: ff647d52-bd32-4945-afa4-5b97d9a0d7dd
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612741(v=office.15)
ms:contentKeyID: 55119792
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f05f6e9199cd474a47d36ff92e255dea92a4d5cc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407554"
---
# <a name="how-do-i-outlook-2013-pia-reference"></a><span data-ttu-id="84b98-102">Comment... (Référence PIA Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="84b98-102">How do I... (Outlook 2013 PIA reference)</span></span>

<span data-ttu-id="84b98-103">Cette section contient des rubriques de tâches procédurales et des exemples de code en Visual Basic et en C\# qui expliquent comment effectuer certaines tâches courantes dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="84b98-103">This section contains procedural tasks topics and code examples in Visual Basic and C# that demonstrate how to perform some common tasks in Microsoft Outlook.</span></span>

<span data-ttu-id="84b98-104">Pour exécuter ces exemples de code, vous devez avoir installé Outlook 2010 et Visual Studio 2008 ou une version ultérieure de ces produits.</span><span class="sxs-lookup"><span data-stu-id="84b98-104">To run these code examples, you must have installed Outlook 2010 and Visual Studio 2008, or a later version of these products.</span></span>

<span data-ttu-id="84b98-105">Vous pouvez utiliser les exemples de codes de cette section sans installer les outils de développement Office pour Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="84b98-105">The code examples in this section do not require that you have installed Office Developer Tools for Visual Studio.</span></span> <span data-ttu-id="84b98-106">Si vous avez besoin d’informations supplémentaires sur l’utilisation des outils, n’hésitez pas à consulter le portail [Prise en main du développement Office](https://developer.microsoft.com/office/docs). Par ailleurs, la page [Solutions Outlook](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) propose d’autres tâches procédurales simples, rédigées en code managé.</span><span class="sxs-lookup"><span data-stu-id="84b98-106">However, you can refer to the [Getting started with Office development](https://developer.microsoft.com/office/docs) portal for information about using the tools, and refer to [Outlook solutions](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) for some basic how-to tasks written in managed code.</span></span>

<span data-ttu-id="84b98-107">Les exemples de code de cette section s’adressent à différents niveaux, du débutant à l’intermédiaire. Certains d’entre eux sont inspirés de l’ouvrage [ Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493) (Programmation d’applications pour Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="84b98-107">Code examples in this section range from the beginner to the intermediate levels, and some of them are adapted from the book [Programming Applications for Microsoft Office Outlook 2007http://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493).</span></span>

<span data-ttu-id="84b98-108">L’équipe Documentation du développeur Office vous invite à communiquer vos idées et vos échantillons de code.</span><span class="sxs-lookup"><span data-stu-id="84b98-108">The Microsoft Office Developer Documentation team welcomes your task ideas and code samples! Topics tagged by the</span></span> <span data-ttu-id="84b98-109">Si nous utilisons vos exemples de code dans du contenu Outlook, nous identifierons votre travail à l’aide d’une signature et d’un lien vers votre site Web.</span><span class="sxs-lookup"><span data-stu-id="84b98-109">The Microsoft Office Developer Documentation team welcomes your task ideas and code samples. If we use your code samples in Outlook content, we will recognize your work with a byline and a link to your Web site. For more information, contact us at docthis@microsoft.com.</span></span> <span data-ttu-id="84b98-110">Pour plus d’informations, veuillez nous écrire à l’adresse docthis@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="84b98-110">For more information, contact us at docthis@microsoft.com.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="84b98-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="84b98-111">In this section</span></span> 

[<span data-ttu-id="84b98-112">Comptes</span><span class="sxs-lookup"><span data-stu-id="84b98-112">Accounts</span></span>](accounts.md)

- [<span data-ttu-id="84b98-113">Obtenir des informations sur le compte</span><span class="sxs-lookup"><span data-stu-id="84b98-113">Get account information</span></span>](how-to-get-account-information.md)
- [<span data-ttu-id="84b98-114">Créer un élément à envoyer pour un compte spécifique basé sur le dossier actif</span><span class="sxs-lookup"><span data-stu-id="84b98-114">Create a Sendable Item for a Specific Account Based on the Current Folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md)
- [<span data-ttu-id="84b98-115">Obtenir le compte lié à un dossier</span><span class="sxs-lookup"><span data-stu-id="84b98-115">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md)
- [<span data-ttu-id="84b98-116">Obtenir des informations sur plusieurs comptes</span><span class="sxs-lookup"><span data-stu-id="84b98-116">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md)
- <span data-ttu-id="84b98-117">[Envoyer un élément de courrier électronique à l’aide d’un compte Windows Live Hotmail](how-to-send-a-mail-item-by-using-a-hotmail-account.md)</span><span class="sxs-lookup"><span data-stu-id="84b98-117">Uses the [SendUsingAccount](how-to-send-a-mail-item-by-using-a-hotmail-account.md) property to send a mail item by using a Windows Live Hotmail account.</span></span>

[<span data-ttu-id="84b98-118">Administration des compléments</span><span class="sxs-lookup"><span data-stu-id="84b98-118">Add-in Administration</span></span>](add-in-administration.md)

- [<span data-ttu-id="84b98-119">Vérifier si Outlook est une application « Démarrer en un clic » sur un ordinateur</span><span class="sxs-lookup"><span data-stu-id="84b98-119">Determine whether Outlook is a Click-to-Run application on a computer</span></span>](how-to-determine-whether-outlook-is-a-click-to-run-application-on-a-computer.md)


[<span data-ttu-id="84b98-120">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="84b98-120">Address Book</span></span>](address-book.md)

- [<span data-ttu-id="84b98-121">Afficher le carnet d’adresses correspondant à un dossier de Contacts dans la boîte de dialogue Sélectionner des noms</span><span class="sxs-lookup"><span data-stu-id="84b98-121">Display in the Select Names dialog box the address book corresponding to a Contacts folder</span></span>](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)
- [<span data-ttu-id="84b98-122">Identifier la liste d’adresses globale ou un ensemble de listes d’adresses pour un magasin</span><span class="sxs-lookup"><span data-stu-id="84b98-122">Get the Global Address List or a set of address lists for a store</span></span>](how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store.md)
- [<span data-ttu-id="84b98-123">Énumérer les entrées de la liste d’adresses globale</span><span class="sxs-lookup"><span data-stu-id="84b98-123">How to: Enumerate the Entries in the Global Address List</span></span>](how-to-enumerate-the-entries-in-the-global-address-list.md)
- [<span data-ttu-id="84b98-124">Afficher les listes d’adresses pour un profil</span><span class="sxs-lookup"><span data-stu-id="84b98-124">Display the address lists for a profile</span></span>](how-to-display-the-address-lists-for-a-profile.md)

[<span data-ttu-id="84b98-125">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="84b98-125">Appointments</span></span>](appointments.md)

- <span data-ttu-id="84b98-126">[Créer un événement sur toute la journée](how-to-create-an-appointment-that-is-an-all-day-event.md)</span><span class="sxs-lookup"><span data-stu-id="84b98-126">Uses the [AllDayEvent](how-to-create-an-appointment-that-is-an-all-day-event.md) property to create an appointment that is an all-day event.</span></span>
- [<span data-ttu-id="84b98-127">Créer un rendez-vous qui commence dans le fuseau horaire Pacifique et se termine dans le fuseau horaire Est</span><span class="sxs-lookup"><span data-stu-id="84b98-127">How to: Create an Appointment That Starts in the Pacific Time Zone and Ends in the Eastern Time Zone</span></span>](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)
- <span data-ttu-id="84b98-128">[Spécifier différents types de destinataires pour un élément de rendez-vous](how-to-specify-different-recipient-types-for-an-appointment-item.md)</span><span class="sxs-lookup"><span data-stu-id="84b98-128">Uses the [OlMeetingRecipientType](how-to-specify-different-recipient-types-for-an-appointment-item.md) enumeration to specify different recipient types for an appointment item.</span></span>
- [<span data-ttu-id="84b98-129">Créer un rendez-vous périodique selon une périodicité par défaut.</span><span class="sxs-lookup"><span data-stu-id="84b98-129">Creates a recurring appointment by using the default recurrence pattern.</span></span>](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)
- [<span data-ttu-id="84b98-130">Créer un rendez-vous périodique ayant une périodicité hebdomadaire</span><span class="sxs-lookup"><span data-stu-id="84b98-130">Create a recurring appointment that has a weekly pattern</span></span>](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)
- [<span data-ttu-id="84b98-131">Créer un rendez-vous périodique annuel selon une périodicité de toutes les n années</span><span class="sxs-lookup"><span data-stu-id="84b98-131">Create an annual recurring appointment that uses a YearNth pattern</span></span>](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)
- [<span data-ttu-id="84b98-132">Trouver un rendez-vous spécifique dans une série de rendez-vous périodiques</span><span class="sxs-lookup"><span data-stu-id="84b98-132">Find a specific appointment in a recurring appointment series</span></span>](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="84b98-133">Créer une exception de rendez-vous dans une série de rendez-vous périodiques</span><span class="sxs-lookup"><span data-stu-id="84b98-133">Create an exception appointment in a recurring appointment series</span></span>](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="84b98-134">Créer un rappel pour un élément de rendez-vous</span><span class="sxs-lookup"><span data-stu-id="84b98-134">Create a reminder for an appointment item</span></span>](how-to-create-a-reminder-for-an-appointment-item.md)
- [<span data-ttu-id="84b98-135">Importer les données XML de rendez-vous dans les objets de rendez-vous Outlook</span><span class="sxs-lookup"><span data-stu-id="84b98-135">Import Appointment XML Data into Outlook Appointment Objects</span></span>](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)

[<span data-ttu-id="84b98-136">Pièces jointes</span><span class="sxs-lookup"><span data-stu-id="84b98-136">Attachments</span></span>](attachments.md)

- [<span data-ttu-id="84b98-137">Joindre un fichier à un élément de courrier</span><span class="sxs-lookup"><span data-stu-id="84b98-137">Attach a File to a Mail Item</span></span>](https://docs.microsoft.com/office/vba/outlook/How-to/Items-Folders-and-Stores/attach-a-file-to-a-mail-item)
- [<span data-ttu-id="84b98-138">Attacher un élément de Contact Outlook dans un courrier électronique</span><span class="sxs-lookup"><span data-stu-id="84b98-138">Attach an Outlook Contact Item to an Email Message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/attach-an-outlook-contact-item-to-an-email-message)
- [<span data-ttu-id="84b98-139">Limiter la taille d’une pièce jointe à un courrier électronique Outlook</span><span class="sxs-lookup"><span data-stu-id="84b98-139">Limit the Size of an Attachment to an Outlook Email Message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/limit-the-size-of-an-attachment-to-an-outlook-email-message)
- [<span data-ttu-id="84b98-140">Modifier une pièce jointe d’un courrier électronique Outlook</span><span class="sxs-lookup"><span data-stu-id="84b98-140">Modify an Attachment of an Outlook Email Message</span></span>](https://docs.microsoft.com/office/vba/outlook/concepts/attachments/modify-an-attachment-of-an-outlook-email-message)
- [<span data-ttu-id="84b98-141">Supprimer par programme les pièces jointes de niveau 2 de sécurité contenues dans les messages et les enregistrer sur le disque</span><span class="sxs-lookup"><span data-stu-id="84b98-141">Programmatically remove security level 2 attachments from messages and save them to disk</span></span>](how-to-programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk.md)

[<span data-ttu-id="84b98-142">Calendrier</span><span class="sxs-lookup"><span data-stu-id="84b98-142">Calendar</span></span>](calendar.md)

- [<span data-ttu-id="84b98-143">Partager le planning de disponibilité pendant une période spécifiée dans un calendrier</span><span class="sxs-lookup"><span data-stu-id="84b98-143">Share Free/Busy schedule within a specified period in a calendar</span></span>](how-to-share-free-busy-schedule-within-a-specified-period-in-a-calendar.md)
- [<span data-ttu-id="84b98-144">Partager des informations de calendrier par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="84b98-144">Share calendar information through email</span></span>](how-to-share-calendar-information-through-e-mail.md)
- [<span data-ttu-id="84b98-145">Afficher le calendrier partagé d’un destinataire</span><span class="sxs-lookup"><span data-stu-id="84b98-145">Display a shared calendar of a recipient</span></span>](how-to-display-a-shared-calendar-of-a-recipient.md)
- [<span data-ttu-id="84b98-146">Enregistrer un calendrier sur le disque</span><span class="sxs-lookup"><span data-stu-id="84b98-146">Save a calendar to disk</span></span>](how-to-save-a-calendar-to-disk.md)
- [<span data-ttu-id="84b98-147">Ouvrir et afficher le contenu d’un fichier iCalendar</span><span class="sxs-lookup"><span data-stu-id="84b98-147">Open and display the contents of an iCalendar file</span></span>](how-to-open-and-display-the-contents-of-an-icalendar-file.md)

[<span data-ttu-id="84b98-148">Catégories de couleurs</span><span class="sxs-lookup"><span data-stu-id="84b98-148">Color Categories</span></span>](color-categories.md)

- [<span data-ttu-id="84b98-149">Énumérer et ajouter des catégories</span><span class="sxs-lookup"><span data-stu-id="84b98-149">Enumerate and add categories</span></span>](how-to-enumerate-and-add-categories.md)
- [<span data-ttu-id="84b98-150">Affecter des catégories à un élément</span><span class="sxs-lookup"><span data-stu-id="84b98-150">Assign categories to an item</span></span>](how-to-assign-categories-to-an-item.md)

[<span data-ttu-id="84b98-151">Contacts</span><span class="sxs-lookup"><span data-stu-id="84b98-151">Contacts</span></span>](contacts.md)

- [<span data-ttu-id="84b98-152">Créer un élément de Contact</span><span class="sxs-lookup"><span data-stu-id="84b98-152">Create a Contact item</span></span>](how-to-create-a-contact-item.md)
- [<span data-ttu-id="84b98-153">Créer un élément de Contact personnalisé</span><span class="sxs-lookup"><span data-stu-id="84b98-153">Create a custom Contact item</span></span>](how-to-create-a-custom-contact-item.md)
- [<span data-ttu-id="84b98-154">Créer un élément de Contact à partir d’un fichier vCard et enregistrer l’élément dans un dossier</span><span class="sxs-lookup"><span data-stu-id="84b98-154">Create a Contact item from a vCard file and save the item in a folder</span></span>](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)

[<span data-ttu-id="84b98-155">Conversations</span><span class="sxs-lookup"><span data-stu-id="84b98-155">Conversations</span></span>](conversations.md)

- [<span data-ttu-id="84b98-156">Obtenir et afficher les éléments dans une conversation</span><span class="sxs-lookup"><span data-stu-id="84b98-156">Get and display items in a conversation</span></span>](how-to-get-and-display-items-in-a-conversation.md)
- [<span data-ttu-id="84b98-157">Obtenir et énumérer les conversations sélectionnées</span><span class="sxs-lookup"><span data-stu-id="84b98-157">Get and enumerate selected conversations</span></span>](how-to-get-and-enumerate-selected-conversations.md)

[<span data-ttu-id="84b98-158">Cartes de visite électroniques</span><span class="sxs-lookup"><span data-stu-id="84b98-158">Electronic Business Cards</span></span>](electronic-business-cards.md)

- [<span data-ttu-id="84b98-159">Modifier la mise en page d’une carte de visite électronique</span><span class="sxs-lookup"><span data-stu-id="84b98-159">Modify the layout of an electronic business card</span></span>](how-to-modify-the-layout-of-an-electronic-business-card.md)
- [<span data-ttu-id="84b98-160">Envoyer un élément de courrier avec une carte de visite électronique</span><span class="sxs-lookup"><span data-stu-id="84b98-160">Send a mail item with an electronic business card</span></span>](how-to-send-a-mail-item-with-an-electronic-business-card.md)

[<span data-ttu-id="84b98-161">Utilisateurs Exchange</span><span class="sxs-lookup"><span data-stu-id="84b98-161">Exchange Users</span></span>](exchange-users.md)

- [<span data-ttu-id="84b98-162">Informations sur l’utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="84b98-162">Get information about the current login user.</span></span>](how-to-get-information-about-the-current-user.md)
- [<span data-ttu-id="84b98-163">Obtenir des informations sur toutes les listes de distribution dont l’utilisateur actuel est membre</span><span class="sxs-lookup"><span data-stu-id="84b98-163">Get information about all distribution lists of which the current user is a member</span></span>](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)
- [<span data-ttu-id="84b98-164">Créer une liste de distribution</span><span class="sxs-lookup"><span data-stu-id="84b98-164">Create a distribution list</span></span>](how-to-create-a-distribution-list.md)
- [<span data-ttu-id="84b98-165">Obtenir les membres d’une liste de distribution Exchange</span><span class="sxs-lookup"><span data-stu-id="84b98-165">Get members of an Exchange distribution list</span></span>](how-to-get-members-of-an-exchange-distribution-list.md)
- [<span data-ttu-id="84b98-166">Obtenir des informations sur le gestionnaire de l’utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="84b98-166">Get information about the current user's manager</span></span>](how-to-get-information-about-the-current-user-s-manager.md)
- [<span data-ttu-id="84b98-167">Obtenir des informations concernant la disponibilité d’un gestionnaire d’un utilisateur Exchange</span><span class="sxs-lookup"><span data-stu-id="84b98-167">Get availability information for an Exchange user's manager</span></span>](how-to-get-availability-information-for-an-exchange-user-s-manager.md)
- [<span data-ttu-id="84b98-168">Vérifier la réponse d’un gestionnaire à une demande de réunion</span><span class="sxs-lookup"><span data-stu-id="84b98-168">Check a manager's response to a meeting request</span></span>](how-to-check-a-manager-s-response-to-a-meeting-request.md)
- [<span data-ttu-id="84b98-169">Obtenir des informations sur les collaborateurs directs du gestionnaire de l’utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="84b98-169">Get information about direct reports of the current user's manager</span></span>](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md)

[<span data-ttu-id="84b98-170">Dossiers</span><span class="sxs-lookup"><span data-stu-id="84b98-170">Folders</span></span>](folders.md)

- [<span data-ttu-id="84b98-171">Ajouter un dossier à la liste des dossiers</span><span class="sxs-lookup"><span data-stu-id="84b98-171">Add a folder to the folder list</span></span>](how-to-add-a-folder-to-the-folder-list.md)
- [<span data-ttu-id="84b98-172">Énumérer les dossiers</span><span class="sxs-lookup"><span data-stu-id="84b98-172">Enumerate folders</span></span>](how-to-enumerate-folders.md)
- [<span data-ttu-id="84b98-173">Obtenir un dossier par défaut et énumérer ses sous-dossiers</span><span class="sxs-lookup"><span data-stu-id="84b98-173">Get a default folder and enumerate its subfolders</span></span>](how-to-get-a-default-folder-and-enumerate-its-subfolders.md)
- [<span data-ttu-id="84b98-174">Obtenir un dossier à partir de son chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="84b98-174">Get a folder based on its folder path</span></span>](how-to-get-a-folder-based-on-its-folder-path.md)
- [<span data-ttu-id="84b98-175">Sélectionner un dossier et afficher les informations du dossier</span><span class="sxs-lookup"><span data-stu-id="84b98-175">Select a folder and display folder information</span></span>](how-to-select-a-folder-and-display-folder-information.md)
- [<span data-ttu-id="84b98-176">Obtenir la classe de message par défaut d’un dossier</span><span class="sxs-lookup"><span data-stu-id="84b98-176">Get the default message class of a folder</span></span>](how-to-get-the-default-message-class-of-a-folder.md)
- [<span data-ttu-id="84b98-177">Accéder aux données spécifiques à la solution stockées comme message masqué dans un dossier</span><span class="sxs-lookup"><span data-stu-id="84b98-177">Access solution-specific data stored as a hidden message in a folder</span></span>](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)
- [<span data-ttu-id="84b98-178">S’assurer que les propriétés des éléments personnalisés sont prises en charge dans les requêtes au niveau du dossier</span><span class="sxs-lookup"><span data-stu-id="84b98-178">Ensure that custom item properties are supported in folder-level queries</span></span>](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md)

[<span data-ttu-id="84b98-179">Éléments Outlook généraux</span><span class="sxs-lookup"><span data-stu-id="84b98-179">General Outlook items</span></span>](general-outlook-items.md)

- [<span data-ttu-id="84b98-180">Créer une classe d’assistance pour accéder aux membres d’un élément Outlook courant</span><span class="sxs-lookup"><span data-stu-id="84b98-180">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [<span data-ttu-id="84b98-181">Afficher les éléments sélectionnés dans l’Explorateur actif</span><span class="sxs-lookup"><span data-stu-id="84b98-181">Display selected items in the active Explorer</span></span>](how-to-display-selected-items-in-the-active-explorer.md)

[<span data-ttu-id="84b98-182">Partage de groupe</span><span class="sxs-lookup"><span data-stu-id="84b98-182">Group Sharing</span></span>](group-sharing.md)

- [<span data-ttu-id="84b98-183">S’abonner à un flux RSS</span><span class="sxs-lookup"><span data-stu-id="84b98-183">Subscribe to an RSS feed</span></span>](how-to-subscribe-to-an-rss-feed.md)
- [<span data-ttu-id="84b98-184">Synchroniser Outlook avec un dossier SharePoint</span><span class="sxs-lookup"><span data-stu-id="84b98-184">How to: Synchronize Outlook with a SharePoint Folder</span></span>](how-to-synchronize-outlook-with-a-sharepoint-folder.md)

[<span data-ttu-id="84b98-185">Courrier</span><span class="sxs-lookup"><span data-stu-id="84b98-185">Mail</span></span>](mail.md)

- [<span data-ttu-id="84b98-186">Créer un élément de courrier à l’aide d’un modèle de message</span><span class="sxs-lookup"><span data-stu-id="84b98-186">Create a mail item by using a message template</span></span>](how-to-create-a-mail-item-by-using-a-message-template.md)
- [<span data-ttu-id="84b98-187">Créer un élément de courrier, joindre un rapport et envoyer l’élément de courrier au gestionnaire de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="84b98-187">Create a mail item, attach a report, and send the mail item to the user's manager</span></span>](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md)
- [<span data-ttu-id="84b98-188">Envoyer un courrier électronique d’après l’adresse SMTP d’un compte</span><span class="sxs-lookup"><span data-stu-id="84b98-188">Send an E-mail Given the SMTP Address of an Account</span></span>](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md)
- [<span data-ttu-id="84b98-189">Ajouter des options de vote à un élément de courrier</span><span class="sxs-lookup"><span data-stu-id="84b98-189">Add voting options to a mail item</span></span>](how-to-add-voting-options-to-a-mail-item.md)
- [<span data-ttu-id="84b98-190">Ajouter une action personnalisée en guise de réponse à un élément de courrier</span><span class="sxs-lookup"><span data-stu-id="84b98-190">Add a custom action as a response to a mail item</span></span>](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md)
- [<span data-ttu-id="84b98-191">Obtenir l’adresse SMTP de l’expéditeur d’un élément de courrier</span><span class="sxs-lookup"><span data-stu-id="84b98-191">Get the SMTP address of the sender of a mail item</span></span>](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md)
- [<span data-ttu-id="84b98-192">Spécifier différents types de destinataires pour un élément de courrier</span><span class="sxs-lookup"><span data-stu-id="84b98-192">Specify different recipient types for a mail item</span></span>](how-to-specify-different-recipient-types-for-a-mail-item.md)

[<span data-ttu-id="84b98-193">Demandes de réunion</span><span class="sxs-lookup"><span data-stu-id="84b98-193">Meeting Requests</span></span>](meeting-requests.md)

- [<span data-ttu-id="84b98-194">Créer une demande de réunion, ajouter des destinataires et spécifier un emplacement</span><span class="sxs-lookup"><span data-stu-id="84b98-194">Create a meeting request, add recipients, and specify a location</span></span>](how-to-create-a-meeting-request-add-recipients-and-specify-a-location.md)
- [<span data-ttu-id="84b98-195">Obtenir l’organisateur d’une réunion</span><span class="sxs-lookup"><span data-stu-id="84b98-195">Get the organizer of a meeting</span></span>](how-to-get-the-organizer-of-a-meeting.md)
- [<span data-ttu-id="84b98-196">Consulter toutes les réponses à une demande de réunion</span><span class="sxs-lookup"><span data-stu-id="84b98-196">Check all responses to a meeting request</span></span>](how-to-check-all-responses-to-a-meeting-request.md)
- [<span data-ttu-id="84b98-197">Rechercher l’élément de rendez-vous associé à une demande de réunion</span><span class="sxs-lookup"><span data-stu-id="84b98-197">Find the appointment item associated with a meeting request</span></span>](how-to-find-the-appointment-item-associated-with-a-meeting-request.md)
- [<span data-ttu-id="84b98-198">Accepter automatiquement une demande de réunion</span><span class="sxs-lookup"><span data-stu-id="84b98-198">Automatically accept a meeting request</span></span>](how-to-automatically-accept-a-meeting-request.md)
- [<span data-ttu-id="84b98-199">Inviter un utilisateur à répondre à une demande de réunion</span><span class="sxs-lookup"><span data-stu-id="84b98-199">Prompt a user to respond to a meeting request</span></span>](how-to-prompt-a-user-to-respond-to-a-meeting-request.md)

[<span data-ttu-id="84b98-200">Destinataires</span><span class="sxs-lookup"><span data-stu-id="84b98-200">Recipients</span></span>](recipients.md)

- [<span data-ttu-id="84b98-201">Afficher la boîte de dialogue Sélectionner des noms pour résoudre des destinataires</span><span class="sxs-lookup"><span data-stu-id="84b98-201">Display the Select Names dialog box to resolve recipients</span></span>](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)
- [<span data-ttu-id="84b98-202">Utiliser la boîte de dialogue Sélectionner des noms pour obtenir et attribuer des destinataires à un rendez-vous</span><span class="sxs-lookup"><span data-stu-id="84b98-202">Use the Select Names dialog box to obtain and assign recipients to an appointment</span></span>](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)
- [<span data-ttu-id="84b98-203">Obtenir l’adresse de courrier électronique d’un destinataire</span><span class="sxs-lookup"><span data-stu-id="84b98-203">Get the email address of a recipient</span></span>](how-to-get-the-e-mail-address-of-a-recipient.md)

[<span data-ttu-id="84b98-204">Règles</span><span class="sxs-lookup"><span data-stu-id="84b98-204">Rules</span></span>](rules.md)

- [<span data-ttu-id="84b98-205">Créer une règle pour classer les éléments de courrier provenant d’un gestionnaire et les marquer pour assurer un suivi</span><span class="sxs-lookup"><span data-stu-id="84b98-205">Create a rule to file mail items from a manager and flag them for follow-up</span></span>](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)
- [<span data-ttu-id="84b98-206">Exécuter une règle instantanément</span><span class="sxs-lookup"><span data-stu-id="84b98-206">Execute a rule instantly</span></span>](how-to-execute-a-rule-instantly.md)
- [<span data-ttu-id="84b98-207">Exécuter une règle sur un ordinateur local</span><span class="sxs-lookup"><span data-stu-id="84b98-207">Execute a rule on a local computer</span></span>](how-to-execute-a-rule-on-a-local-computer.md)
- [<span data-ttu-id="84b98-208">Créer une règle pour affecter des catégories aux éléments de courrier en fonction de plusieurs mots dans l’objet</span><span class="sxs-lookup"><span data-stu-id="84b98-208">Create a rule to assign categories to mail items based on multiple words in the subject</span></span>](how-to-create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject.md)


[<span data-ttu-id="84b98-209">Exemples de tâches utilisant des événements Outlook</span><span class="sxs-lookup"><span data-stu-id="84b98-209">Sample Tasks Using Outlook Events</span></span>](sample-tasks-using-outlook-events.md)

- [<span data-ttu-id="84b98-210">Mettre en œuvre un wrapper pour les inspecteurs et suivre les événements au niveau des éléments dans chaque inspecteur</span><span class="sxs-lookup"><span data-stu-id="84b98-210">Implement a Wrapper for Inspectors and Track Item-Level Events in Each Inspector</span></span>](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)

[<span data-ttu-id="84b98-211">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="84b98-211">Search and Filter</span></span>](search-and-filter.md)

- [<span data-ttu-id="84b98-212">Filtrer et énumérer efficacement les éléments d’un dossier</span><span class="sxs-lookup"><span data-stu-id="84b98-212">Filter and efficiently enumerate items in a folder</span></span>](how-to-filter-and-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="84b98-213">Utiliser SetColumns pour énumérer efficacement les éléments d’un dossier</span><span class="sxs-lookup"><span data-stu-id="84b98-213">Use SetColumns to efficiently enumerate items in a folder</span></span>](how-to-use-setcolumns-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="84b98-214">Utiliser les tableaux pour énumérer efficacement les éléments d’un dossier</span><span class="sxs-lookup"><span data-stu-id="84b98-214">Use arrays to efficiently enumerate items in a folder</span></span>](how-to-use-arrays-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="84b98-215">Énumérer les éléments dans la Boîte de réception en fonction de l’heure de la dernière modification</span><span class="sxs-lookup"><span data-stu-id="84b98-215">Enumerate items in the Inbox based on the last modification time</span></span>](how-to-enumerate-items-in-the-inbox-based-on-the-last-modification-time.md)
- [<span data-ttu-id="84b98-216">Filtrer et afficher les éléments de Boîte de réception modifiés le mois dernier</span><span class="sxs-lookup"><span data-stu-id="84b98-216">Filter and display Inbox items modified in the last month</span></span>](how-to-filter-and-display-inbox-items-modified-in-the-last-month.md)
- [<span data-ttu-id="84b98-217">Filtrer et afficher des propriétés à plusieurs valeurs lors de l’énumération d’éléments dans un dossier</span><span class="sxs-lookup"><span data-stu-id="84b98-217">Filter and display multivalued properties when enumerating items in a folder</span></span>](how-to-filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="84b98-218">Filtrer et afficher des propriétés calculées lors de l’énumération d’éléments dans un dossier</span><span class="sxs-lookup"><span data-stu-id="84b98-218">This example shows how to filter and display computed properties when enumerating items in a folder.</span></span>](how-to-filter-and-display-computed-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="84b98-219">Énumérer les éléments masqués d’un dossier</span><span class="sxs-lookup"><span data-stu-id="84b98-219">Enumerate hidden items in a folder</span></span>](how-to-enumerate-hidden-items-in-a-folder.md)
- [<span data-ttu-id="84b98-220">Utiliser la recherche instantanée pour effectuer une recherche dans tous les dossiers et tous les magasins pour une expression dans l’objet</span><span class="sxs-lookup"><span data-stu-id="84b98-220">Use instant search to search all folders and all stores for a phrase in the subject</span></span>](how-to-use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject.md)
- [<span data-ttu-id="84b98-221">Rechercher une expression dans le corps d’éléments d’un dossier</span><span class="sxs-lookup"><span data-stu-id="84b98-221">Search for a phrase in the body of items in a folder</span></span>](how-to-search-for-a-phrase-in-the-body-of-items-in-a-folder.md)
- [<span data-ttu-id="84b98-222">Rechercher les pièces jointes des éléments d’un dossier pour une expression exacte</span><span class="sxs-lookup"><span data-stu-id="84b98-222">Search attachments of items in a folder for an exact phrase</span></span>](how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase.md)
- [<span data-ttu-id="84b98-223">Effectuer des recherches et obtenir des rendez-vous dans un intervalle de temps</span><span class="sxs-lookup"><span data-stu-id="84b98-223">Search and obtain appointments in a time range</span></span>](how-to-search-and-obtain-appointments-in-a-time-range.md)
- [<span data-ttu-id="84b98-224">Filtrer les rendez-vous périodiques et rechercher une chaîne dans l’objet</span><span class="sxs-lookup"><span data-stu-id="84b98-224">Filter recurring appointments and search for a string in the subject</span></span>](how-to-filter-recurring-appointments-and-search-for-a-string-in-the-subject.md)
- [<span data-ttu-id="84b98-225">Rechercher et obtenir des éléments dans une vue agrégée</span><span class="sxs-lookup"><span data-stu-id="84b98-225">Search and Obtain Items in an Aggregated View</span></span>](how-to-search-and-obtain-items-in-an-aggregated-view.md)

[<span data-ttu-id="84b98-226">Sessions</span><span class="sxs-lookup"><span data-stu-id="84b98-226">Sessions</span></span>](sessions.md)

- [<span data-ttu-id="84b98-227">Obtenir et se connecter à une instance d’Outlook</span><span class="sxs-lookup"><span data-stu-id="84b98-227">Get and sign in to an instance of Outlook</span></span>](how-to-get-and-log-on-to-an-instance-of-outlook.md)

[<span data-ttu-id="84b98-228">Magasins</span><span class="sxs-lookup"><span data-stu-id="84b98-228">Stores</span></span>](stores.md)

- [<span data-ttu-id="84b98-229">Obtenir des informations sur les magasins dans un profil</span><span class="sxs-lookup"><span data-stu-id="84b98-229">Get information about stores in a profile</span></span>](how-to-get-information-about-stores-in-a-profile.md)
- [<span data-ttu-id="84b98-230">Ajouter ou supprimer un magasin</span><span class="sxs-lookup"><span data-stu-id="84b98-230">Add or remove a store</span></span>](how-to-add-or-remove-a-store.md)

[<span data-ttu-id="84b98-231">Tâches</span><span class="sxs-lookup"><span data-stu-id="84b98-231">Tasks</span></span>](tasks.md)

- [<span data-ttu-id="84b98-232">Créer un élément de tâche</span><span class="sxs-lookup"><span data-stu-id="84b98-232">Create a new task</span></span>](how-to-create-a-task-item.md)
- [<span data-ttu-id="84b98-233">Affecter une tâche à un destinataire</span><span class="sxs-lookup"><span data-stu-id="84b98-233">Assign a task to a recipient</span></span>](how-to-assign-a-task-to-a-recipient.md)
- [<span data-ttu-id="84b98-234">Afficher les éléments de demande de tâche envoyés à un destinataire</span><span class="sxs-lookup"><span data-stu-id="84b98-234">Display the task request items sent to a recipient</span></span>](how-to-display-the-task-request-items-sent-to-a-recipient.md)
- [<span data-ttu-id="84b98-235">Répondre à un élément de demande de tâche</span><span class="sxs-lookup"><span data-stu-id="84b98-235">Respond to a task request item</span></span>](how-to-respond-to-a-task-request-item.md)
- [<span data-ttu-id="84b98-236">Créer une tâche périodique</span><span class="sxs-lookup"><span data-stu-id="84b98-236">Create a recurring task</span></span>](how-to-create-a-recurring-task.md)
- [<span data-ttu-id="84b98-237">Marquer les éléments de courrier provenant d’un gestionnaire pour assurer un suivi</span><span class="sxs-lookup"><span data-stu-id="84b98-237">Flag mail items from a manager for follow-up</span></span>](how-to-flag-mail-items-from-a-manager-for-follow-up.md)

[<span data-ttu-id="84b98-238">Affichages</span><span class="sxs-lookup"><span data-stu-id="84b98-238">Views</span></span>](views.md)

- [<span data-ttu-id="84b98-239">Créer un affichage</span><span class="sxs-lookup"><span data-stu-id="84b98-239">Create a view</span></span>](how-to-create-a-view.md)
- [<span data-ttu-id="84b98-240">Ajouter des champs à un affichage</span><span class="sxs-lookup"><span data-stu-id="84b98-240">Add fields to a view</span></span>](how-to-add-fields-to-a-view.md)
- [<span data-ttu-id="84b98-241">Énumérer les éléments d’un affichage tableau</span><span class="sxs-lookup"><span data-stu-id="84b98-241">Enumerate items in a table view</span></span>](how-to-enumerate-items-in-a-table-view.md)



