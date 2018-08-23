---
title: Garantir une notification thread-safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ad10b2ebd835b21f207fd43ecd8aebc7e1f475f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585303"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="7c743-103">Garantir une notification thread-safe</span><span class="sxs-lookup"><span data-stu-id="7c743-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="7c743-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c743-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c743-105">Si votre client s’exécute sur une plate-forme multithread, vous devrez peut-être pour l’assurance que les appels vers les méthodes [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) se produisent sur un thread particulier.</span><span class="sxs-lookup"><span data-stu-id="7c743-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="7c743-106">Étant donné que les appels vers **OnNotify** peuvent se produire généralement sur n’importe quel thread, il est possible de recevoir des notifications sur des threads inattendus et indésirables conduisant à des erreurs sont difficiles à déboguer.</span><span class="sxs-lookup"><span data-stu-id="7c743-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="7c743-107">Afin de garantir que les appels vers **OnNotify** pour une notification particulier sont effectuées sur le même thread qui a été utilisé pour les **notifications** d' appel, appelez [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) avant d’appeler des **notifications**.</span><span class="sxs-lookup"><span data-stu-id="7c743-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="7c743-108">\*\* \*\* HrThisThreadAdviseSink \*\*\* crée un nouvel objet de récepteur de notifications à partir de votre objet de récepteur advise.</span><span class="sxs-lookup"><span data-stu-id="7c743-108">** **HrThisThreadAdviseSink**** creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="7c743-109">Transmettez ce nouvel objet dans l’appel à **Advise**.</span><span class="sxs-lookup"><span data-stu-id="7c743-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="7c743-110">Tous les clients avec des objets qui risque de ne pas fonctionner en dehors du contexte d’un thread particulier doivent toujours enregistrer de récepteur de notifications de notification objets récepteur créés avec **HrThisThreadAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="7c743-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

