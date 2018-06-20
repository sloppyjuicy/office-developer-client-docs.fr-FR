---
title: Tables de destinataires de codage à l’aide du format TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 8110eff9b38c76023621f34396d65714a4316d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783260"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="55439-103">Tables de destinataires de codage à l’aide du format TNEF</span><span class="sxs-lookup"><span data-stu-id="55439-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="55439-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="55439-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="55439-105">Le type de codage d’un tableau de destinataire dans le flux TNEF est rarement nécessaire dans la mesure où les systèmes de messagerie plus en charge les listes de destinataires directement.</span><span class="sxs-lookup"><span data-stu-id="55439-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="55439-106">En règle générale, les propriétés du destinataire sont transmises dans l’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="55439-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="55439-107">Lors de l’inclusion de la table de destinataires est nécessaire, TNEF peut coder la table du destinataire dans le cadre de son traitement normal.</span><span class="sxs-lookup"><span data-stu-id="55439-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="55439-108">Cette opération est effectuée pendant la phase initiale du traitement TNEF.</span><span class="sxs-lookup"><span data-stu-id="55439-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="55439-109">Le fournisseur de transport peut inclure la table des destinataires du message en appelant la méthode [ITnef::AddProps](itnef-addprops.md) avec la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) spécifiée dans la liste d’inclusion.</span><span class="sxs-lookup"><span data-stu-id="55439-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="55439-110">Obtient la table de destinataires du message, TNEF interroge l’ensemble de colonnes et traite chaque ligne du tableau dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="55439-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="55439-111">Une autre méthode est disponible si le fournisseur de transport a besoin de modifier la table de destinataires avant le codage.</span><span class="sxs-lookup"><span data-stu-id="55439-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="55439-112">Le fournisseur de transport peut construire la table nécessaire, puis appelez la méthode [ITnef::EncodeRecips](itnef-encoderecips.md) .</span><span class="sxs-lookup"><span data-stu-id="55439-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="55439-113">Si NULL est indiqué dans le paramètre _lpRecipTable_ , la table de destinataires provient directement à partir du message comme indiqué pour **ITnef::AddProps**.</span><span class="sxs-lookup"><span data-stu-id="55439-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

