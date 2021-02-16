---
title: Garantie d’une Thread-Safe notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424846"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="89a37-103">Garantie d’une Thread-Safe notification</span><span class="sxs-lookup"><span data-stu-id="89a37-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="89a37-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89a37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89a37-105">Si votre client s’exécute sur une plateforme multithread, vous devrez peut-être vous assurer que les appels à vos méthodes [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) se produisent sur un thread particulier.</span><span class="sxs-lookup"><span data-stu-id="89a37-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="89a37-106">Étant donné que les appels **à OnNotify** peuvent généralement se produire sur n’importe quel thread, il est possible de recevoir des notifications sur des threads inattendus et indésirables, entraînant des erreurs difficiles à déboguer.</span><span class="sxs-lookup"><span data-stu-id="89a37-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="89a37-107">Pour garantir que les appels à **OnNotify** pour une notification particulière  sont effectués sur le même thread que celui utilisé pour l’appel advise, appelez [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) avant d’appeler **Advise**.</span><span class="sxs-lookup"><span data-stu-id="89a37-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="89a37-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* crée un nouvel objet de sink de conseil à partir de votre objet de sink de conseil.</span><span class="sxs-lookup"><span data-stu-id="89a37-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="89a37-109">Passez ce nouvel objet dans l’appel de **Advise**.</span><span class="sxs-lookup"><span data-stu-id="89a37-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="89a37-110">Tous les clients avec des objets de sink de conseil qui peuvent ne pas fonctionner en dehors du contexte d’un thread particulier doivent toujours inscrire les objets de sink de conseil créés avec **HrThisThreadAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="89a37-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

