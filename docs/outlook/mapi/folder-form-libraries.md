---
title: Bibliothèques de formulaires de dossier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ec12cf567dbbd8c1710f835a3c19369dd3626fd4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281556"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="02ab7-103">Bibliothèques de formulaires de dossier</span><span class="sxs-lookup"><span data-stu-id="02ab7-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="02ab7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02ab7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02ab7-105">Dans certains cas, vous souhaiterez peut-être associer un ou plusieurs formulaires à un dossier spécifique.</span><span class="sxs-lookup"><span data-stu-id="02ab7-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="02ab7-106">Par exemple, les employés de votre organisation peuvent disposer d'un dossier de rapport de progression dans leur banque de messages personnelle pour créer et stocker des rapports d'avancement.</span><span class="sxs-lookup"><span data-stu-id="02ab7-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="02ab7-107">Étant donné que le rapport de progression est propre au dossier de rapports d'avancement de chaque utilisateur, il peut ne pas être approprié de stocker le formulaire de rapport d'avancement dans la bibliothèque de formulaires système.</span><span class="sxs-lookup"><span data-stu-id="02ab7-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="02ab7-108">Toutefois, une copie du formulaire de rapport de progression peut être conservée dans le tableau des contenus associés du dossier des rapports d'avancement de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="02ab7-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="02ab7-109">Cela empêche l'utilisateur d'utiliser les formulaires de rapport de progression en dehors du dossier désigné.</span><span class="sxs-lookup"><span data-stu-id="02ab7-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="02ab7-110">D'un plan conceptuel, il existe une bibliothèque de formulaires de dossier pour chaque dossier dans une banque de messages, même si aucun serveur de formulaires n'est installé dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="02ab7-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="02ab7-111">Les bibliothèques de formulaires de dossier sont implémentées comme les autres bibliothèques de formulaires; elles sont stockées en tant que tables de contenu associées dans l'autre partie du dossier.</span><span class="sxs-lookup"><span data-stu-id="02ab7-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="02ab7-112">Étant donné que les bibliothèques de formulaires de dossier sont contenues dans le dossier, elles sont copiées avec leur dossier parent dans les opérations de copie.</span><span class="sxs-lookup"><span data-stu-id="02ab7-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="02ab7-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02ab7-113">See also</span></span>



[<span data-ttu-id="02ab7-114">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="02ab7-114">MAPI Forms</span></span>](mapi-forms.md)

