---
title: Comptes
TOCTitle: Accounts
ms:assetid: 28df6dbd-4d24-42f3-91c1-fd8b3a4ea722
ms:mtpsurl: https://msdn.microsoft.com/library/office/ff184597(v=office.15)
ms:contentKeyID: 55119790
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d539f38419a8eaac60cd3054da6283a49bf4cc00
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723011"
---
# <a name="accounts"></a><span data-ttu-id="a29d1-102">Comptes</span><span class="sxs-lookup"><span data-stu-id="a29d1-102">Accounts</span></span> 

<span data-ttu-id="a29d1-103">Cette section fournit des exemples de tâches qui impliquent des comptes de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a29d1-103">This section provides sample tasks that involve email accounts.</span></span> <span data-ttu-id="a29d1-104">Microsoft Exchange Server, POP3 (Post Office Protocol 3), IMAP (Internet Message Access Protocol) et les comptes HTTP sont des exemples de compte de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a29d1-104">Examples of email accounts are Microsoft Exchange Server, Post Office Protocol 3 (POP3), Internet Message Access Protocol (IMAP), and Hypertext Transfer Protocol (HTTP) accounts.</span></span> <span data-ttu-id="a29d1-105">Le compte du profil actuel est représenté par un objet [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia).</span><span class="sxs-lookup"><span data-stu-id="a29d1-105">An account for the current profile is represented by an [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia) object.</span></span>


|<span data-ttu-id="a29d1-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="a29d1-106">Topic</span></span>|<span data-ttu-id="a29d1-107">Description</span><span class="sxs-lookup"><span data-stu-id="a29d1-107">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="a29d1-108">Obtention des informations du compte</span><span class="sxs-lookup"><span data-stu-id="a29d1-108">Get account information</span></span>](how-to-get-account-information.md) | <span data-ttu-id="a29d1-109">Prend comme argument d'entrée un objet Microsoft Outlook [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) approuvé, et utilise l'objet **Account** pour afficher les détails de chaque compte disponible pour le profil Outlook actuel.</span><span class="sxs-lookup"><span data-stu-id="a29d1-109">Takes as an input argument a trusted Microsoft Outlook [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) object, and uses the **Account** object to display the details of each account that is available for the current Outlook profile.</span></span>|
|[<span data-ttu-id="a29d1-110">Création d’un élément à envoyer pour un compte spécifique basé sur le dossier actuel</span><span class="sxs-lookup"><span data-stu-id="a29d1-110">Create a sendable item for a specific account based on the current folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md) | <span data-ttu-id="a29d1-111">Contient deux exemples de code qui montrent comment créer un élément de messagerie à envoyer et une demande de réunion, et comment les envoyer en utilisant un compte spécifique basé sur le dossier actuel.</span><span class="sxs-lookup"><span data-stu-id="a29d1-111">Contains two code examples that show how to create a sendable email item and meeting request, and then send them by using a specific account that is based on the current folder.</span></span>|
|[<span data-ttu-id="a29d1-112">Obtention du compte lié à un dossier</span><span class="sxs-lookup"><span data-stu-id="a29d1-112">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md) | <span data-ttu-id="a29d1-113">Obtient le compte associé à un dossier dans la session actuelle.</span><span class="sxs-lookup"><span data-stu-id="a29d1-113">Gets the account that is associated with a folder in the current session.</span></span>|
|[<span data-ttu-id="a29d1-114">Obtention des informations de plusieurs comptes</span><span class="sxs-lookup"><span data-stu-id="a29d1-114">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md) | <span data-ttu-id="a29d1-115">Obtient et affiche des informations diverses sur chaque compte dans le profil actuel.</span><span class="sxs-lookup"><span data-stu-id="a29d1-115">Obtains and displays miscellaneous information about each account in the current profile.</span></span>|
|[<span data-ttu-id="a29d1-116">Envoi d’un élément de courrier électronique avec un compte Hotmail</span><span class="sxs-lookup"><span data-stu-id="a29d1-116">Send a mail item by using a Hotmail account</span></span>](how-to-send-a-mail-item-by-using-a-hotmail-account.md) | <span data-ttu-id="a29d1-117">Utilise la propriété [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) pour envoyer un message en utilisant un compte Windows Live Hotmail.</span><span class="sxs-lookup"><span data-stu-id="a29d1-117">Uses the [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) property to send a mail item by using a Windows Live Hotmail account.</span></span>|

## <a name="see-also"></a><span data-ttu-id="a29d1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a29d1-118">See also</span></span>

- [<span data-ttu-id="a29d1-119">Utilisateurs Exchange</span><span class="sxs-lookup"><span data-stu-id="a29d1-119">Exchange users</span></span>](exchange-users.md)
- [<span data-ttu-id="a29d1-120">Courrier</span><span class="sxs-lookup"><span data-stu-id="a29d1-120">Mail</span></span>](mail.md)
- [<span data-ttu-id="a29d1-121">Destinataires</span><span class="sxs-lookup"><span data-stu-id="a29d1-121">Recipients</span></span>](recipients.md)
- [<span data-ttu-id="a29d1-122">Procédure (Référence PIA Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="a29d1-122">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

