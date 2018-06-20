---
title: Noms des dossiers à l’aide de chaînes de caractères
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a6ea37bf573dab996b5a8fd7886a76fddd5b98ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784908"
---
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="d250c-103">Noms des dossiers à l’aide de chaînes de caractères</span><span class="sxs-lookup"><span data-stu-id="d250c-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="d250c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d250c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d250c-105">Si vous accédez à un ou plusieurs dossiers fréquemment pendant une session, envisagez d’attribution de noms aux dossiers avec la méthode [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) .</span><span class="sxs-lookup"><span data-stu-id="d250c-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="d250c-106">Bien que **IMsgStore::SetReceiveFolder** est utilisé essentiellement pour établir des dossiers spéciaux pour recevoir les messages entrants pour les classes de message particulier, il peut également servir pour associer un dossier avec un nom.</span><span class="sxs-lookup"><span data-stu-id="d250c-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="d250c-107">Le nom peut être identique à la classe de message, ou elle peut être une chaîne de caractères, personnalisée pour l’utilisation de votre client.</span><span class="sxs-lookup"><span data-stu-id="d250c-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="d250c-108">Association d’un nom à un dossier réduit le temps que nécessaire pour rechercher et ouvrir le dossier.</span><span class="sxs-lookup"><span data-stu-id="d250c-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

