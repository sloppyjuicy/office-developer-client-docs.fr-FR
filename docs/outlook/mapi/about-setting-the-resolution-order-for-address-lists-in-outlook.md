---
title: � propos de la d�finition de l'ordre de r�solution des listes d'adresses dans Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: cfc640fd419ad030de6922fa61817881caa70d07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782842"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="bbb69-103">� propos de la d�finition de l'ordre de r�solution des listes d'adresses dans Outlook</span><span class="sxs-lookup"><span data-stu-id="bbb69-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="bbb69-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bbb69-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bbb69-105">Pour chaque profil, Microsoft Office Outlook prend en charge plusieurs listes d’adresses et les utilisateurs peuvent spécifier manuellement l’ordre des listes d’adresses par les destinataires de courrier électronique messages et les participants dans les demandes de réunion sont résolus.</span><span class="sxs-lookup"><span data-stu-id="bbb69-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="bbb69-106">Par exemple, vous pouvez d�finir l'ordre de r�solution afin que les noms sont r�solus tout d'abord par rapport � votre carnet d'adresses Outlook, puis par rapport � la liste d'adresses globale.</span><span class="sxs-lookup"><span data-stu-id="bbb69-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="bbb69-107">Sur un ordinateur, un utilisateur peut ouvrir le carnet d'adresses, cliquez sur **Outils**, puis sur **Options** pour sp�cifier l'ordre de r�solution.</span><span class="sxs-lookup"><span data-stu-id="bbb69-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="bbb69-108">Toutefois, dans un environnement d'entreprise, il est plus efficace pour les administrateurs informatiques � d�finir par programme l'ordre des listes d'adresses par lequel les noms sont r�solus.</span><span class="sxs-lookup"><span data-stu-id="bbb69-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="bbb69-109">Ce code peut �tre utilis� dans le cadre d'un script d'automation de d�marrage par un administrateur � l'int�rieur de l'entreprise.</span><span class="sxs-lookup"><span data-stu-id="bbb69-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="bbb69-p102">MAPI prend en charge la m�thode **[SetSearchPath](iaddrbook-getsearchpath.md)** dans l'interface **[IAddrBook](iaddrbookimapiprop.md)**, qui vous permet de d�finir un nouveau chemin d'acc�s de la recherche dans le profil qui est utilis� pour la r�solution de nom. Pour utiliser la m�thode **IAddrBook::SetSearchPath**, vous devez sp�cifier l'ordre de r�solution de votre choix � l'aide d'un tableau qui contient les conteneurs de l'adresse appropri�e de la documentation dans l'ordre, qu'ils doivent �tre r�solus. Chaque entr�e dans ce tableau doit �galement contenir l'identificateur d'entr�e du carnet d'adresses correspondant.</span><span class="sxs-lookup"><span data-stu-id="bbb69-p102">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="bbb69-113">Voici des exemples de code montrant comment sp�cifier un chemin de recherche personnalis� pour les listes d'adresses.</span><span class="sxs-lookup"><span data-stu-id="bbb69-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="bbb69-114">Définir par programme l’ordre de résolution des listes d’adresses</span><span class="sxs-lookup"><span data-stu-id="bbb69-114">Programmatically Set the Resolution Order for Address Lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="bbb69-115">KB 292590 : comment faire pour modifier l'ordre de tri de carnet d'adresses avec SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="bbb69-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](http://support.microsoft.com/kb/292590)
    

