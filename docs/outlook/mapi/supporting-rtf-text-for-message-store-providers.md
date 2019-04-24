---
title: Prise en charge du texte RTF pour les fournisseurs de banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349615"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a><span data-ttu-id="431f9-103">Prise en charge du texte RTF pour les fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="431f9-103">Supporting RTF Text for Message Store Providers</span></span>

  
  
<span data-ttu-id="431f9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="431f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="431f9-105">Certaines applications clientes permettent aux utilisateurs d'utiliser du texte RTF (Rich Text Format) dans leurs messages.</span><span class="sxs-lookup"><span data-stu-id="431f9-105">Some client applications allow users to use Rich Text Format (RTF) text in their messages.</span></span> <span data-ttu-id="431f9-106">Si votre fournisseur de banque de messages doit prendre en charge le texte RTF dans les messages, il doit gérer la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), en plus de la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="431f9-106">If your message store provider needs to support RTF text in messages, it needs to handle the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, in addition to the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span> <span data-ttu-id="431f9-107">En premier lieu, cela signifie de stocker les deux propriétés et de s'assurer que **PR_BODY** contient une version en texte brut du texte dans **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="431f9-107">Primarily, this means storing both properties, and making sure that **PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="431f9-108">La fonction [RTFSync](rtfsync.md) est utile à cette fin.</span><span class="sxs-lookup"><span data-stu-id="431f9-108">The [RTFSync](rtfsync.md) function is useful for this purpose.</span></span> 
  
<span data-ttu-id="431f9-109">Deux indicateurs peuvent être définis dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de l'objet Banque de messages qui indique aux clients ce qu'ils peuvent attendre du fournisseur de banque de messages par rapport au **PR_BODY** et à **PR_ Propriétés RTF_COMPRESSED** sur les messages dans la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="431f9-109">There are two flags that can be set in the message store object's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property that tell clients what they can expect from the message store provider with respect to the **PR_BODY** and **PR_RTF_COMPRESSED** properties on messages in the message store.</span></span> <span data-ttu-id="431f9-110">L'indicateur STORE_RTF_OK indique que la Banque peut générer de manière dynamique la valeur de la propriété **PR_BODY** à partir de la propriété **PR_RTF_COMPRESSED** , ce qui évite aux clients de procéder à leur synchronisation de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="431f9-110">The STORE_RTF_OK flag indicates that the store can generate the value of the **PR_BODY** property from the **PR_RTF_COMPRESSED** property dynamically, which relieves clients from the burden of synchronizing them explicitly.</span></span> <span data-ttu-id="431f9-111">L'indicateur STORE_UNCOMPRESSED_RTF indique que le fournisseur de banque de messages peut prendre en charge des données non compressées dans **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="431f9-111">The STORE_UNCOMPRESSED_RTF flag indicates that the message store provider can support uncompressed data in **PR_RTF_COMPRESSED**.</span></span>
  
<span data-ttu-id="431f9-112">Les fournisseurs de banques de messages qui ne prennent pas en charge le texte RTF doivent supprimer la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) lorsque la propriété **PR_BODY** est modifiée afin d'interagir correctement avec les applications clientes qui prennent en charge le texte RTF .</span><span class="sxs-lookup"><span data-stu-id="431f9-112">Message store providers that do not support RTF text need to delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property when the **PR_BODY** property changes in order to interoperate properly with client applications that do support RTF text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="431f9-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="431f9-113">See also</span></span>



[<span data-ttu-id="431f9-114">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="431f9-114">Message Store Features</span></span>](message-store-features.md)

