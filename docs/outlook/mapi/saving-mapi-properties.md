---
title: L’enregistrement des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6135dfae915a1e70743f9224352390c4b56ea02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787041"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="93a52-103">L’enregistrement des propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="93a52-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="93a52-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="93a52-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="93a52-105">De nombreux objets prennent en charge un modèle de transaction de traitement selon laquelle les modifications apportées aux propriétés ne sont pas apportées définitive jusqu'à ce qu’ils soient validées à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="93a52-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="93a52-106">Tandis que les modifications apportées aux propriétés sont gérées par les méthodes [IMAPIProp::SetProps](imapiprop-setprops.md) et [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) , l’étape de validation est gérée par [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="93a52-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="93a52-107">Il n’est pas qu’après un appel réussi **SaveChanges** que la version la plus récente des propriétés d’un objet est accessible.</span><span class="sxs-lookup"><span data-stu-id="93a52-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="93a52-108">Lorsque **l’argument SaveChanges** renvoie la valeur d’erreur MAPI_E_OBJECT_CHANGED, il s’agit d’un avertissement indiquant qu’un autre client est validation simultanément des modifications à l’objet.</span><span class="sxs-lookup"><span data-stu-id="93a52-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="93a52-109">Il est possible, selon le fournisseur de l’implémentation de l’objet, permettant aux clients plusieurs correctement ouvrir un objet en appelant la méthode **OpenEntry** avec l’indicateur n’est défini, en leur donnant accès en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="93a52-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="93a52-110">L’objet est renvoyé à partir de ces qu'un appel **OpenEntry** est une capture instantanée des données de stockage.</span><span class="sxs-lookup"><span data-stu-id="93a52-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="93a52-111">Toute tentative ultérieure pour modifier ces données peut remplacer la tentative précédente.</span><span class="sxs-lookup"><span data-stu-id="93a52-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="93a52-112">Lors de la réception MAPI_E_OBJECT_CHANGED de **SaveChanges**, un client a la possibilité de :</span><span class="sxs-lookup"><span data-stu-id="93a52-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="93a52-113">Effectuez une copie de l’objet pour contenir les modifications.</span><span class="sxs-lookup"><span data-stu-id="93a52-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="93a52-114">Appeler un autre **SaveChanges**, spécifiant FORCE_SAVE.</span><span class="sxs-lookup"><span data-stu-id="93a52-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="93a52-115">Appel de **SaveChanges** avec l’indicateur FORCE_SAVE remplace l’enregistrement précédent et modifie d’un client définitive.</span><span class="sxs-lookup"><span data-stu-id="93a52-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93a52-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93a52-116">See also</span></span>



[<span data-ttu-id="93a52-117">Vue d'ensemble de la propri�t� MAPI</span><span class="sxs-lookup"><span data-stu-id="93a52-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

