---
title: Utilisation des objets thread-safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 49a94b785a51b4b0c3082832145250eec0745a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580977"
---
# <a name="using-thread-safe-objects"></a><span data-ttu-id="7a09c-103">Utilisation des objets thread-safe</span><span class="sxs-lookup"><span data-stu-id="7a09c-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="7a09c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a09c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a09c-105">Les applications clientes peuvent supposent que les objets utilisés directement ou en tant que rappels sont toujours thread-safe, sauf dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="7a09c-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="7a09c-106">Objet d’état d’un fournisseur de transport obtenu par un appel de client à [IMAPISession::OpenEntry](imapisession-openentry.md) avec un identificateur d’entrée à partir de la ligne de tableau de statut du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7a09c-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="7a09c-107">Tous les objets de formulaire MAPI obtenus par un appel de client à [MAPIOpenFormMgr](mapiopenformmgr.md).</span><span class="sxs-lookup"><span data-stu-id="7a09c-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="7a09c-108">Objets de formulaire respecter les règles du modèle apartment et les clients doivent utiliser les et tous les objets contenus dans les uniquement sur le thread qui a créé les.</span><span class="sxs-lookup"><span data-stu-id="7a09c-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="7a09c-109">Lorsqu’un client accède à la ligne d’un fournisseur de transport dans la table d’état qui inclut l’identificateur d’entrée de l’objet associé à l’état, le client peut appeler **OpenEntry** avec cet identificateur d’entrée pour ouvrir l’objet d’état.</span><span class="sxs-lookup"><span data-stu-id="7a09c-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="7a09c-110">Cet objet état n’est pas thread-safe, car les fournisseurs de transport s’exécutent dans le contexte du spouleur MAPI et ne conservent pas d’un contexte distinct pour l’objet de leur état.</span><span class="sxs-lookup"><span data-stu-id="7a09c-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="7a09c-111">L’objet état se conforme aux règles du modèle apartment et clients doivent utiliser uniquement sur le thread qui l’a créé.</span><span class="sxs-lookup"><span data-stu-id="7a09c-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="7a09c-112">Un client doit également appeler [exécuter MAPIInitialize](mapiinitialize.md) sur chaque thread avant d’utiliser tous les objets MAPI et [MAPIUninitialize](mapiuninitialize.md) lorsque cette utilisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="7a09c-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="7a09c-113">Ces appels doivent être effectuées, même si les objets utilisés sont transmis à la thread d’une source externe.</span><span class="sxs-lookup"><span data-stu-id="7a09c-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="7a09c-114">**Exécuter MAPIInitialize** et **MAPIUninitialize** peuvent être appelées à partir de n’importe où à l’exception à partir d’une fonction Win32 **DllMain** , une fonction qui est appelée par le système lorsque les processus et les threads sont initialisés et arrêtés ou lors des appels vers le ** LoadLibrary** et fonctions **FreeLibrary** .</span><span class="sxs-lookup"><span data-stu-id="7a09c-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="7a09c-115">Objets utilisation indirecte doivent jamais considéré comme thread-safe.</span><span class="sxs-lookup"><span data-stu-id="7a09c-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="7a09c-116">Utilisation indirecte objets sont retournés par les méthodes qui nécessitent des pointeurs d’interface destination comme paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7a09c-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="7a09c-117">Exemples de ces méthodes sont **IMAPIProp::CopyTo** et **CopyProps**, **IMAPIFolder::CopyFolder** et **CopyMessage**et **IMsgServiceAdmin::CopyMsgService**.</span><span class="sxs-lookup"><span data-stu-id="7a09c-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="7a09c-118">Si un fournisseur de services souhaite appeler ce type d’objet à partir d’un thread différent de celui sur lequel il a été passé, le fournisseur est chargé de marshaling explicite de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7a09c-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  

