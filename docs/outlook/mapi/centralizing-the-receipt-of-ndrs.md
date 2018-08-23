---
title: Centralisation de la réception de rapports de non-remise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 16a150105211231af54ccfdc5d1565aeecea729e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579437"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="723ac-103">Centralisation de la réception de rapports de non-remise</span><span class="sxs-lookup"><span data-stu-id="723ac-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="723ac-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="723ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="723ac-105">**Pour que les rapports de non-remise (NDR) arrive à un emplacement central lorsque plusieurs instances de votre client exécutent simultanément**</span><span class="sxs-lookup"><span data-stu-id="723ac-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="723ac-106">Les valeurs appropriées pour le compte qui doit recevoir la valeur **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) et **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) les rapports.</span><span class="sxs-lookup"><span data-stu-id="723ac-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="723ac-107">Créer l’identificateur d’entrée en appelant [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="723ac-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="723ac-108">Comprendre les systèmes de messagerie qui ne tient pas compte le compte que vous avez demandé pour les rapports et les envoyez à l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="723ac-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="723ac-109">Réduisez l’impact qu’il aura sur administrateurs que vous devrez déplacer les rapports :</span><span class="sxs-lookup"><span data-stu-id="723ac-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="723ac-110">Donner à votre message d’origine à une classe de message distinctes, par exemple IPM. Note.MSNNews.</span><span class="sxs-lookup"><span data-stu-id="723ac-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="723ac-111">Rechercher les messages entrants avec la classe Report.IPM.Note.MSNNews.NDR et les transférer vers le compte que vous avez l’intention de rapports placés au premier.</span><span class="sxs-lookup"><span data-stu-id="723ac-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="723ac-112">En même temps, envoyer à un système de messagerie ignorée votre compte de rapport de non-remise pour communiquer qu’il doit respecter la propriété **PR_REPORT_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="723ac-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="723ac-113">Les systèmes de messagerie plus qui n’effectue pas de **PR_REPORT_ENTRYID** pas respecte les conventions de classe de message MAPI soit.</span><span class="sxs-lookup"><span data-stu-id="723ac-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="723ac-114">Par conséquent, vous serez invité à quelque chose qui ressemble à une note.</span><span class="sxs-lookup"><span data-stu-id="723ac-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="723ac-115">Il s’agit d’un peu plus difficile à gérer, car l’entrée est donc variable.</span><span class="sxs-lookup"><span data-stu-id="723ac-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="723ac-116">Examinez l’objet et le transmet si vous trouvez soit quelque chose à partir d’une liste de mots que moyenne « non remis » ou quelque chose à partir de l’objet d’origine.</span><span class="sxs-lookup"><span data-stu-id="723ac-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="723ac-117">Préparez-vous à régler ces listes au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="723ac-117">Be prepared to tune these lists over time.</span></span> 
    

