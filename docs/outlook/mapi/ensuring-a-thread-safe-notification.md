---
title: Assurer une Notification de Thread-Safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 70e594057f2d654e0527b0caa0951e44842df809
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783250"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="afae7-103">Assurer une Notification de Thread-Safe</span><span class="sxs-lookup"><span data-stu-id="afae7-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="afae7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="afae7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="afae7-105">Si votre client s’exécute sur une plate-forme multithread, vous devrez peut-être pour l’assurance que les appels vers les méthodes [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) se produisent sur un thread particulier.</span><span class="sxs-lookup"><span data-stu-id="afae7-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="afae7-106">Étant donné que les appels vers **OnNotify** peuvent se produire généralement sur n’importe quel thread, il est possible de recevoir des notifications sur des threads inattendus et indésirables conduisant à des erreurs sont difficiles à déboguer.</span><span class="sxs-lookup"><span data-stu-id="afae7-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="afae7-107">Afin de garantir que les appels vers **OnNotify** pour une notification particulier sont effectuées sur le même thread qui a été utilisé pour les **notifications** d' appel, appelez [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) avant d’appeler des **notifications**.</span><span class="sxs-lookup"><span data-stu-id="afae7-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="afae7-108">\*\* \*\* HrThisThreadAdviseSink \*\*\* crée un nouvel objet de récepteur de notifications à partir de votre objet de récepteur advise.</span><span class="sxs-lookup"><span data-stu-id="afae7-108">** **HrThisThreadAdviseSink**** creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="afae7-109">Transmettez ce nouvel objet dans l’appel à **Advise**.</span><span class="sxs-lookup"><span data-stu-id="afae7-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="afae7-110">Tous les clients avec des objets qui risque de ne pas fonctionner en dehors du contexte d’un thread particulier doivent toujours enregistrer de récepteur de notifications de notification objets récepteur créés avec **HrThisThreadAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="afae7-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

