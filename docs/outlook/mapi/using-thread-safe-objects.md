---
title: Utilisation d'objets thread-safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 611e0a49f0fd8df8fe40205a33ed5501055c3d45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425168"
---
# <a name="using-thread-safe-objects"></a><span data-ttu-id="3acda-103">Utilisation d'objets thread-safe</span><span class="sxs-lookup"><span data-stu-id="3acda-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="3acda-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3acda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3acda-105">Les applications clientes peuvent supposer que les objets utilisés directement ou en tant que rappels sont toujours thread-safe, sauf dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="3acda-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="3acda-106">Objet d'état d'un fournisseur de transport obtenu via un appel client vers [IMAPISession:: OpenEntry](imapisession-openentry.md) avec un identificateur d'entrée de la ligne de la table d'État du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3acda-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="3acda-107">Tous les objets de formulaire MAPI obtenus par le biais d'un appel client vers [MAPIOpenFormMgr](mapiopenformmgr.md).</span><span class="sxs-lookup"><span data-stu-id="3acda-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="3acda-108">Les objets Form obéissent aux règles de modèle cloisonné et les clients doivent les utiliser et tous les objets qu'ils contiennent uniquement sur le thread qui les a créés.</span><span class="sxs-lookup"><span data-stu-id="3acda-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="3acda-109">Lorsqu'un client accède à la ligne d'un fournisseur de transport dans la table d'État qui contient l'identificateur d'entrée de l'objet d'état associé, le client peut appeler **OpenEntry** avec cet identificateur d'entrée pour ouvrir l'objet d'État.</span><span class="sxs-lookup"><span data-stu-id="3acda-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="3acda-110">Cet objet Status n'est pas thread-safe car les fournisseurs de transport s'exécutent dans le contexte du spouleur MAPI et ne gèrent pas de contexte distinct pour leur objet d'État.</span><span class="sxs-lookup"><span data-stu-id="3acda-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="3acda-111">L'objet Status obéit aux règles de modèle cloisonné et les clients ne doivent l'utiliser que sur le thread qui l'a créé.</span><span class="sxs-lookup"><span data-stu-id="3acda-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="3acda-112">Un client doit également appeler [MAPIInitialize](mapiinitialize.md) sur chaque thread avant d'utiliser les objets MAPI et [MAPIUninitialize](mapiuninitialize.md) lorsque cette utilisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="3acda-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="3acda-113">Ces appels doivent être effectués même si les objets à utiliser sont transmis au thread à partir d'une source externe.</span><span class="sxs-lookup"><span data-stu-id="3acda-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="3acda-114">**MAPIInitialize** et **MAPIUninitialize** peuvent être appelés depuis n'importe quel endroit, sauf à partir d'une fonction **DllMain** Win32, d'une fonction appelée par le système lorsque les processus et les **threads sont initialisés et terminés, ou lorsque des appels au Fonctions LoadLibrary** et **FreeLibrary** .</span><span class="sxs-lookup"><span data-stu-id="3acda-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="3acda-115">Les objets d'utilisation inDirecte ne doivent jamais être considérés comme thread-safe.</span><span class="sxs-lookup"><span data-stu-id="3acda-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="3acda-116">Les objets use inDirects sont renvoyés par les méthodes qui nécessitent des pointeurs d'interface de destination comme paramètres d'entrée.</span><span class="sxs-lookup"><span data-stu-id="3acda-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="3acda-117">Les exemples de ces méthodes sont **IMAPIProp:: CopyTo** et **CopyProps**, **IMAPIFolder:: CopyFolder** et **CopyMessage**, et **IMsgServiceAdmin:: CopyMsgService**.</span><span class="sxs-lookup"><span data-stu-id="3acda-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="3acda-118">Si un fournisseur de services souhaite appeler ce type d'objet à partir d'un autre thread que celui sur lequel il a été passé, le fournisseur est chargé de marshaler explicitement l'objet.</span><span class="sxs-lookup"><span data-stu-id="3acda-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  

