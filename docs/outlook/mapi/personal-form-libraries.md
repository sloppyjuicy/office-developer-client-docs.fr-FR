---
title: Bibliothèques de formulaires personnels
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c84665077f9c8e02647a4d348042515366b0c090
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348446"
---
# <a name="personal-form-libraries"></a><span data-ttu-id="22296-103">Bibliothèques de formulaires personnels</span><span class="sxs-lookup"><span data-stu-id="22296-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="22296-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22296-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22296-105">Comme son nom l'indique, les bibliothèques de formulaires personnels contiennent des formulaires intéressants pour un utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="22296-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="22296-106">La bibliothèque de formulaires personnels d'un utilisateur est la bibliothèque de formulaires associée à la Banque de messages par défaut identifiée dans le profil de l'utilisateur; chaque profil installé sur une station de travail peut utiliser une banque par défaut distincte et, par conséquent, une bibliothèque de formulaires personnels distincte.</span><span class="sxs-lookup"><span data-stu-id="22296-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="22296-107">Une bibliothèque de formulaires personnels peut contenir des copies de formulaires qui sont également contenus dans d'autres bibliothèques de formulaires en plus d'autres formulaires.</span><span class="sxs-lookup"><span data-stu-id="22296-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="22296-108">Une bibliothèque de formulaires personnels est implémentée dans la table des contenus associés du dossier racine de la Banque de messages par défaut d'un utilisateur (qu'elle réside sur un serveur ou localement sur la station de travail de l'utilisateur).</span><span class="sxs-lookup"><span data-stu-id="22296-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="22296-109">Si la Banque de messages par défaut de l'utilisateur est stockée sur la station de travail de l'utilisateur, les bibliothèques de formulaires personnels offrent des performances améliorées en permettant aux applications d'accéder aux formulaires localement plutôt qu'au réseau.</span><span class="sxs-lookup"><span data-stu-id="22296-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="22296-110">Il met également les formulaires à la disposition des utilisateurs qui travaillent en mode hors connexion, ce qui peut se produire lorsque les utilisateurs souhaitent prendre leur forme sur des ordinateurs portables et s'ils ne disposent pas d'un accès à un réseau.</span><span class="sxs-lookup"><span data-stu-id="22296-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="22296-111">Les propriétés et l'implémentation sous-jacente d'entrées de bibliothèque de formulaires personnelles incluent une propriété «ID de conteneur» qui identifie un conteneur maître avec lequel l'entrée locale doit être synchronisée.</span><span class="sxs-lookup"><span data-stu-id="22296-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="22296-112">Il peut s'agir de l'identificateur d'un dossier arbitraire qui contient des formulaires.</span><span class="sxs-lookup"><span data-stu-id="22296-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="22296-113">Cette fonctionnalité est utile si vous utilisez un gestionnaire de formulaires personnalisés qui prend en charge un type de bibliothèque de formulaires à l'échelle de l'Organisation; le gestionnaire de formulaires s'occupe de synchroniser les formulaires stockés dans la bibliothèque de formulaires personnels et la bibliothèque de formulaires à l'échelle de l'organisation.</span><span class="sxs-lookup"><span data-stu-id="22296-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="22296-114">Cela se produit probablement lorsque le gestionnaire de formulaire a été chargé, mais peut théoriquement se produire à tout moment.</span><span class="sxs-lookup"><span data-stu-id="22296-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="22296-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22296-115">See also</span></span>



[<span data-ttu-id="22296-116">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="22296-116">MAPI Forms</span></span>](mapi-forms.md)

