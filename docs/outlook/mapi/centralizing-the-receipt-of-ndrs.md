---
title: Centralisation de la réception des notifications d’échec de remise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: af2531076755d1e183409f50fe1a0c97d28063f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405855"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="79d62-103">Centralisation de la réception des notifications d’échec de remise</span><span class="sxs-lookup"><span data-stu-id="79d62-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="79d62-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79d62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79d62-105">**Pour que les rapports de non-delivery arrivent à un emplacement central lorsque plusieurs instances de votre client sont en cours d’exécution simultanément**</span><span class="sxs-lookup"><span data-stu-id="79d62-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="79d62-106">Définissez **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) et **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) sur les valeurs appropriées pour le compte qui doit recevoir les rapports.</span><span class="sxs-lookup"><span data-stu-id="79d62-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="79d62-107">Créez l’identificateur d’entrée en appelant [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="79d62-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="79d62-108">Comprenez qu’il existe des systèmes de messagerie qui ignorent le compte que vous avez demandé pour les rapports et les envoient à l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="79d62-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="79d62-109">Réduisez l’impact que cela aura sur les administrateurs qui devront déplacer des rapports en :</span><span class="sxs-lookup"><span data-stu-id="79d62-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="79d62-110">Donner à votre message d’origine une classe de message distincte, telle qu’IPM. Note.MSNNews.</span><span class="sxs-lookup"><span data-stu-id="79d62-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="79d62-111">Recherchez les messages entrants avec class Report.IPM.Note.MSNNews.NDR et transfertz-les vers le compte vers qui vous souhaitez envoyer des rapports.</span><span class="sxs-lookup"><span data-stu-id="79d62-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="79d62-112">En même temps, envoyez un courrier électronique au système de messagerie qui a ignoré votre compte de rapport de non-envoi pour signaler qu’il doit respecter la **propriété PR_REPORT_ENTRYID.**</span><span class="sxs-lookup"><span data-stu-id="79d62-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="79d62-113">La plupart des systèmes de messagerie qui ne respectent **pas PR_REPORT_ENTRYID** respectent pas non plus les conventions de classe de message MAPI.</span><span class="sxs-lookup"><span data-stu-id="79d62-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="79d62-114">Par conséquent, vous recevrez un message qui ressemble à une note.</span><span class="sxs-lookup"><span data-stu-id="79d62-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="79d62-115">Cette opération est un peu plus difficile à gérer, car l’entrée est très variable.</span><span class="sxs-lookup"><span data-stu-id="79d62-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="79d62-116">Regardez l’objet et faites-le avancer si vous trouvez quelque chose dans une liste de mots qui signifie « non transmis » ou quelque chose de votre objet d’origine.</span><span class="sxs-lookup"><span data-stu-id="79d62-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="79d62-117">Soyez prêt à régler ces listes au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="79d62-117">Be prepared to tune these lists over time.</span></span> 
    

