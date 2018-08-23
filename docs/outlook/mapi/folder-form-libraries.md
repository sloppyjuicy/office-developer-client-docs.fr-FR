---
title: Bibliothèques de formulaires de dossiers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f95aa26d6104da657c6ae6ab0c449d45c073223a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580550"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="1521d-103">Bibliothèques de formulaires de dossiers</span><span class="sxs-lookup"><span data-stu-id="1521d-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="1521d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1521d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1521d-105">Dans certains cas, vous souhaitez associer un ou plusieurs formulaires à un dossier spécifique.</span><span class="sxs-lookup"><span data-stu-id="1521d-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="1521d-106">Par exemple, les employés de votre organisation pourraient s’un dossier de rapport de progression dans leur banque de messages personnels pour la création et le stockage des rapports de progression.</span><span class="sxs-lookup"><span data-stu-id="1521d-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="1521d-107">Étant donné que le rapport de progression est spécifique à un dossier de rapport de progression de chaque utilisateur, il n’est peut-être pas approprié stocker le formulaire de rapport de progression dans la bibliothèque de formulaires à l’échelle du système.</span><span class="sxs-lookup"><span data-stu-id="1521d-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="1521d-108">Toutefois, une copie du formulaire de rapport de progression permettre être conservée dans la table de contenu associée du dossier de rapport de progression de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1521d-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="1521d-109">Cela empêche l’utilisateur d’utiliser des formulaires de rapport d’avancement en dehors du dossier désigné.</span><span class="sxs-lookup"><span data-stu-id="1521d-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="1521d-110">De façon conceptuelle, il est une bibliothèque de formulaires de dossier pour tous les dossiers dans une banque de messages, même si aucun serveur de formulaire n’est installés dans ce.</span><span class="sxs-lookup"><span data-stu-id="1521d-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="1521d-111">Bibliothèques de formulaires dossier sont implémentées comme autres bibliothèques de formulaires, elles sont stockées en tant que tables de contenu associé dans le composant de substitution du dossier.</span><span class="sxs-lookup"><span data-stu-id="1521d-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="1521d-112">Étant donné que les bibliothèques de formulaires dossier sont contenus dans le dossier, ils sont copiés ainsi que dans les opérations de copie de leur dossier parent.</span><span class="sxs-lookup"><span data-stu-id="1521d-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1521d-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1521d-113">See also</span></span>



[<span data-ttu-id="1521d-114">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="1521d-114">MAPI Forms</span></span>](mapi-forms.md)

