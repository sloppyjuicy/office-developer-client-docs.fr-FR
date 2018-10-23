---
title: À propos de la définition de l’ordre de résolution pour les listes d’adresses dans Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Dernière modification : 05 juillet 2012'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391408"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="e8cf9-103">À propos de la définition de l’ordre de résolution pour les listes d’adresses dans Outlook</span><span class="sxs-lookup"><span data-stu-id="e8cf9-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="e8cf9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8cf9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8cf9-105">Pour chaque profil, Microsoft Office Outlook prend en charge plusieurs listes d’adresses et les utilisateurs peuvent indiquer manuellement l’ordre des listes d’adresses dans lequel les destinataires des messages électroniques et les participants inclus dans les demandes de réunion sont résolus.</span><span class="sxs-lookup"><span data-stu-id="e8cf9-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in e-mail messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="e8cf9-106">Par exemple, vous pouvez définir l’ordre de résolution afin que les noms soient résolus en premier par rapport à votre carnet d’adresses Outlook, puis par rapport à la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="e8cf9-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="e8cf9-107">Sur un ordinateur, un utilisateur peut ouvrir le carnet d’adresses, cliquer sur **Outils**, puis sur **Options** pour indiquer l’ordre de résolution.</span><span class="sxs-lookup"><span data-stu-id="e8cf9-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="e8cf9-108">Toutefois, dans un environnement d’entreprise, la solution la plus efficace pour les administrateurs informatiques consiste à définir par programmation l’ordre des listes d’adresses dans lequel les noms sont résolus.</span><span class="sxs-lookup"><span data-stu-id="e8cf9-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="e8cf9-109">Ce type de code peut être utilisé dans le cadre d’un script d’automatisation du démarrage qu’un administrateur déploie au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="e8cf9-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="e8cf9-p102">MAPI prend en charge la méthode **[SetSearchPath](iaddrbook-getsearchpath.md)** dans l’interface **[IAddrBook](iaddrbookimapiprop.md)**, ce qui vous permet de définir un nouveau chemin de recherche dans le profil utilisé pour la résolution de noms. Pour utiliser la méthode **IAddrBook::SetSearchPath**, vous devez indiquer l’ordre de résolution de votre choix à l’aide d’un tableau qui conserve les conteneurs des carnets d’adresses pertinents dans l’ordre dans lequel ils doivent être résolus. Chaque entrée de ce tableau doit également contenir l’ID d’entrée du carnet d’adresses correspondant.</span><span class="sxs-lookup"><span data-stu-id="e8cf9-p102">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="e8cf9-113">Voici quelques exemples de code de spécification de chemin de recherche personnalisé pour les listes d’adresses.</span><span class="sxs-lookup"><span data-stu-id="e8cf9-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="e8cf9-114">Programmation de l’ordre de résolution des listes d’adresses</span><span class="sxs-lookup"><span data-stu-id="e8cf9-114">Programmatically set the resolution order for address lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="e8cf9-115">Article 292590 de la base de connaissances : Procédure de modification de l’ordre de tri d’un carnet d’adresses avec SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="e8cf9-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](https://support.microsoft.com/kb/292590)
    

