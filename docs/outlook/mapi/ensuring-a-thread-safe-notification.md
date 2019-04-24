---
title: Vérification de la notification thread-safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316584"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="a7876-103">Vérification de la notification thread-safe</span><span class="sxs-lookup"><span data-stu-id="a7876-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="a7876-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7876-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7876-105">Si votre client s'exécute sur une plateforme multithread, vous aurez peut-être besoin de votre assurance que les appels à vos méthodes [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) se produisent sur un thread particulier.</span><span class="sxs-lookup"><span data-stu-id="a7876-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="a7876-106">Étant donné que les appels vers **OnNotify** peuvent généralement se produire sur n'importe quel thread, il est possible de recevoir des notifications sur des threads inattendus et indésirables, conduisant à des erreurs difficiles à déboguer.</span><span class="sxs-lookup"><span data-stu-id="a7876-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="a7876-107">Pour garantir que les appels vers **OnNotify** pour une notification particulière sont effectués sur le même thread que celui utilisé pour l'appel de la méthode Advise, appelez [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) avant d'appeler \*\*\*\* Advise. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a7876-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="a7876-108">\* \* \* \* HrThisThreadAdviseSink \* \* \* \* crée un nouvel objet récepteur de notifications à partir de votre objet récepteur de Conseil.</span><span class="sxs-lookup"><span data-stu-id="a7876-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="a7876-109">TransMettez ce nouvel objet dans l'appel \*\*\*\* à Advise.</span><span class="sxs-lookup"><span data-stu-id="a7876-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="a7876-110">Tous les clients disposant de récepteurs de notifications qui risquent de ne pas fonctionner en dehors du contexte d'un thread particulier doivent toujours enregistrer les objets de récepteur d'avis créés avec **HrThisThreadAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="a7876-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

