---
title: Prise en charge de texte RTF pour les fournisseurs de banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d7d64c8a7d4df4898502f4574ca879c736547b37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787316"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a><span data-ttu-id="bd6b5-103">Prise en charge de texte RTF pour les fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="bd6b5-103">Supporting RTF Text for Message Store Providers</span></span>

  
  
<span data-ttu-id="bd6b5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd6b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd6b5-105">Certaines applications de client permettent aux utilisateurs d’utiliser le texte RTF (RICH Text Format) dans leurs messages.</span><span class="sxs-lookup"><span data-stu-id="bd6b5-105">Some client applications allow users to use Rich Text Format (RTF) text in their messages.</span></span> <span data-ttu-id="bd6b5-106">Si votre message stocker le fournisseur doit prendre en charge de texte RTF dans les messages, il doit gérer la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), en plus de la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bd6b5-106">If your message store provider needs to support RTF text in messages, it needs to handle the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, in addition to the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span> <span data-ttu-id="bd6b5-107">Cela signifie principalement, stockant les deux propriétés et à s’assurer que **PR_BODY** contient une version en texte brut du texte **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="bd6b5-107">Primarily, this means storing both properties, and making sure that **PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="bd6b5-108">La fonction [RTFSync](rtfsync.md) est utile à cet effet.</span><span class="sxs-lookup"><span data-stu-id="bd6b5-108">The [RTFSync](rtfsync.md) function is useful for this purpose.</span></span> 
  
<span data-ttu-id="bd6b5-109">Il existe deux indicateurs peuvent être définies dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de l’objet de banque de messages qui indiquent les clients à ce qu’ils attendent à partir du fournisseur de magasin de message en ce qui concerne les **PR_BODY** et **PR_ RTF_COMPRESSED** propriétés sur les messages dans la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="bd6b5-109">There are two flags that can be set in the message store object's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property that tell clients what they can expect from the message store provider with respect to the **PR_BODY** and **PR_RTF_COMPRESSED** properties on messages in the message store.</span></span> <span data-ttu-id="bd6b5-110">L’indicateur STORE_RTF_OK indique que le magasin peut générer la valeur de la propriété **PR_BODY** à partir de la propriété **PR_RTF_COMPRESSED** dynamiquement, qui permet de clients à partir de la charge de la synchronisation explicitement.</span><span class="sxs-lookup"><span data-stu-id="bd6b5-110">The STORE_RTF_OK flag indicates that the store can generate the value of the **PR_BODY** property from the **PR_RTF_COMPRESSED** property dynamically, which relieves clients from the burden of synchronizing them explicitly.</span></span> <span data-ttu-id="bd6b5-111">L’indicateur STORE_UNCOMPRESSED_RTF indique que le fournisseur de banque de message peut prendre en charge des données non compressées dans **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="bd6b5-111">The STORE_UNCOMPRESSED_RTF flag indicates that the message store provider can support uncompressed data in **PR_RTF_COMPRESSED**.</span></span>
  
<span data-ttu-id="bd6b5-112">Les fournisseurs de magasins de message qui ne prennent pas en charge le texte RTF nécessaire de supprimer la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) lorsque la propriété **PR_BODY** change afin de fonctionner correctement avec les applications clientes qui ne prennent pas en charge le texte RTF .</span><span class="sxs-lookup"><span data-stu-id="bd6b5-112">Message store providers that do not support RTF text need to delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property when the **PR_BODY** property changes in order to interoperate properly with client applications that do support RTF text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd6b5-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd6b5-113">See also</span></span>



[<span data-ttu-id="bd6b5-114">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="bd6b5-114">Message Store Features</span></span>](message-store-features.md)

