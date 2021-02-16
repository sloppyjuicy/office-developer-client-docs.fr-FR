---
title: Enregistrement des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425889"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="783a3-103">Enregistrement des propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="783a3-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="783a3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="783a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="783a3-105">De nombreux objets sont pris en charge par un modèle de traitement de transaction dans lequel les modifications apportées aux propriétés ne sont pas définitives tant qu’elles n’ont pas été apportées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="783a3-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="783a3-106">Alors que les modifications apportées aux propriétés sont gérées par les méthodes [IMAPIProp::SetProps](imapiprop-setprops.md) et [IMAPIProp::D eleteProps,](imapiprop-deleteprops.md) l’étape de validation est gérée par [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="783a3-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="783a3-107">Ce n’est qu’après un appel réussi à **SaveChanges** que la version la plus récente des propriétés d’un objet est accessible.</span><span class="sxs-lookup"><span data-stu-id="783a3-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="783a3-108">Lorsque **SaveChanges renvoie** la valeur d’MAPI_E_OBJECT_CHANGED, il s’agit d’un avertissement signalant qu’un autre client validation simultanément les modifications apportées à l’objet.</span><span class="sxs-lookup"><span data-stu-id="783a3-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="783a3-109">Selon le fournisseur qui implémente l’objet, plusieurs clients peuvent ouvrir un objet en appelant sa méthode **OpenEntry** avec l’indicateur MAPI_MODIFY, ce qui leur donne un accès en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="783a3-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="783a3-110">L’objet renvoyé par un appel **OpenEntry** de ce type est un instantané des données de stockage.</span><span class="sxs-lookup"><span data-stu-id="783a3-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="783a3-111">Chaque tentative ultérieure de modification de ces données peut modifier la tentative précédente.</span><span class="sxs-lookup"><span data-stu-id="783a3-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="783a3-112">Lors de la MAPI_E_OBJECT_CHANGED de **SaveChanges,** un client a la possibilité de :</span><span class="sxs-lookup"><span data-stu-id="783a3-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="783a3-113">Faites une copie de l’objet pour contenir les modifications.</span><span class="sxs-lookup"><span data-stu-id="783a3-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="783a3-114">Effectuer un autre appel **à SaveChanges,** en spécifiant FORCE_SAVE.</span><span class="sxs-lookup"><span data-stu-id="783a3-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="783a3-115">**L’appel de SaveChanges** FORCE_SAVE l’indicateur précédent a la place de l’enregistrer précédent et rend permanentes les modifications d’un client.</span><span class="sxs-lookup"><span data-stu-id="783a3-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="783a3-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="783a3-116">See also</span></span>



[<span data-ttu-id="783a3-117">Vue d’ensemble de la propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="783a3-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

