---
title: Bibliothèques de formulaires personnels
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c84665077f9c8e02647a4d348042515366b0c090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420408"
---
# <a name="personal-form-libraries"></a><span data-ttu-id="8cdba-103">Bibliothèques de formulaires personnels</span><span class="sxs-lookup"><span data-stu-id="8cdba-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="8cdba-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8cdba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8cdba-105">Comme son nom l’indique, les bibliothèques de formulaires personnels contiennent des formulaires d’intérêt pour un utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="8cdba-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="8cdba-106">La bibliothèque de formulaires personnels d’un utilisateur est la bibliothèque de formulaires associée à la magasin de messages par défaut identifiée dans le profil de l’utilisateur . chaque profil installé sur une station de travail peut utiliser un magasin par défaut distinct, et par conséquent, une bibliothèque de formulaires personnelle distincte.</span><span class="sxs-lookup"><span data-stu-id="8cdba-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="8cdba-107">Une bibliothèque de formulaires personnels peut contenir des copies de formulaires qui sont également contenues dans d’autres bibliothèques de formulaires en plus d’autres formulaires.</span><span class="sxs-lookup"><span data-stu-id="8cdba-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="8cdba-108">Une bibliothèque de formulaires personnels est implémentée dans la table des contenus associés du dossier racine dans la magasin de messages par défaut d’un utilisateur , que celle-ci réside sur un serveur ou localement sur la station de travail de l’utilisateur soit sans importance.</span><span class="sxs-lookup"><span data-stu-id="8cdba-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="8cdba-109">Si la boutique de messages par défaut de l’utilisateur est stockée sur la station de travail de l’utilisateur, les bibliothèques de formulaires personnels offrent des performances améliorées en permettant aux applications d’accéder aux formulaires localement plutôt que sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="8cdba-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="8cdba-110">Il met également les formulaires à la disposition des utilisateurs qui travaillent hors connexion, ce qui peut se produire lorsque les utilisateurs souhaitent prendre leurs formulaires avec eux sur des ordinateurs portables et qu’ils n’ont pas accès à un réseau.</span><span class="sxs-lookup"><span data-stu-id="8cdba-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="8cdba-111">Les propriétés et l’implémentation sous-jacente des entrées de bibliothèque de formulaires personnels incluent une propriété « Container ID » qui identifie un conteneur maître avec qui l’entrée locale doit être synchronisée.</span><span class="sxs-lookup"><span data-stu-id="8cdba-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="8cdba-112">Il peut s’agit de l’identificateur d’un dossier arbitraire qui contient des formulaires.</span><span class="sxs-lookup"><span data-stu-id="8cdba-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="8cdba-113">Cela est utile si vous utilisez un gestionnaire de formulaires personnalisé qui prend en charge une sorte de bibliothèque de formulaires à l’échelle de l’organisation ; Le gestionnaire de formulaires se charge de synchroniser les formulaires stockés dans la bibliothèque de formulaires personnels et la bibliothèque de formulaires à l’échelle de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="8cdba-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="8cdba-114">Cela se produira probablement lors du chargement du gestionnaire de formulaires, mais peut théoriquement se produire à tout moment.</span><span class="sxs-lookup"><span data-stu-id="8cdba-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8cdba-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cdba-115">See also</span></span>



[<span data-ttu-id="8cdba-116">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="8cdba-116">MAPI Forms</span></span>](mapi-forms.md)

