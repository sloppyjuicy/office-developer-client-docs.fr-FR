---
title: Codage des tables de destinataires à l'aide de TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339402"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="0b011-103">Codage des tables de destinataires à l'aide de TNEF</span><span class="sxs-lookup"><span data-stu-id="0b011-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="0b011-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b011-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b011-105">Le codage d'une table de destinataires dans le flux TNEF est rarement nécessaire dans la mesure où la plupart des systèmes de messagerie prennent en charge directement les listes de destinataires.</span><span class="sxs-lookup"><span data-stu-id="0b011-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="0b011-106">En règle générale, les propriétés du destinataire sont transmises dans l'en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="0b011-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="0b011-107">Lorsque l'inclusion de la table de destinataires est nécessaire, TNEF peut coder la table de destinataires dans le cadre de son traitement habituel.</span><span class="sxs-lookup"><span data-stu-id="0b011-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="0b011-108">Cette opération est réalisée lors de la phase initiale du traitement TNEF.</span><span class="sxs-lookup"><span data-stu-id="0b011-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="0b011-109">Le fournisseur de transport peut inclure la table de destinataires du message en appelant la méthode [ITnef:: AddProps](itnef-addprops.md) avec la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) spécifiée dans la liste d'inclusion.</span><span class="sxs-lookup"><span data-stu-id="0b011-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="0b011-110">TNEF obtient le tableau de destinataires du message, interroge le jeu de colonnes et traite chaque ligne de la table dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="0b011-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="0b011-111">Une autre méthode est disponible si le fournisseur de transport doit modifier la table de destinataires avant d'être codée.</span><span class="sxs-lookup"><span data-stu-id="0b011-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="0b011-112">Le fournisseur de transport peut construire la table nécessaire, puis appeler la méthode [ITnef:: EncodeRecips](itnef-encoderecips.md) .</span><span class="sxs-lookup"><span data-stu-id="0b011-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="0b011-113">Si la valeur NULL est transmise au paramètre _lpRecipTable_ , la table de destinataires est alors directement extraite du message comme décrit pour **ITnef:: AddProps**.</span><span class="sxs-lookup"><span data-stu-id="0b011-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

