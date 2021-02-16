---
title: Démarrage d’une session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d88ce382b6a6b5f98ec5f88c4deb1565d3b60151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336343"
---
# <a name="starting-a-mapi-session"></a><span data-ttu-id="47243-103">Démarrage d’une session MAPI</span><span class="sxs-lookup"><span data-stu-id="47243-103">Starting a MAPI Session</span></span>

  
  
<span data-ttu-id="47243-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47243-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47243-105">Bien qu’une quantité importante de travail soit effectuée au démarrage de la session, les tâches requises sont minimes.</span><span class="sxs-lookup"><span data-stu-id="47243-105">Although there is a significant amount of work performed during session start up, the required tasks are minimal.</span></span> <span data-ttu-id="47243-106">Une grande partie de ce travail est effectuée dans le traitement MAPI des appels [MAPIInitialize](mapiinitialize.md) et [MAPILogonEx.](mapilogonex.md)</span><span class="sxs-lookup"><span data-stu-id="47243-106">Much of this work is done in the MAPI processing of the [MAPIInitialize](mapiinitialize.md) and [MAPILogonEx](mapilogonex.md) calls.</span></span> <span data-ttu-id="47243-107">Ces deux fonctions acceptent des indicateurs comme paramètres d’entrée pour contrôler des aspects de la session tels que la gestion des notifications et l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="47243-107">Both of these functions accept flags as input parameters for controlling aspects of the session such as notification handling and the user interface.</span></span> <span data-ttu-id="47243-108">Il est important de comprendre les conséquences de la définition de chacun de ces indicateurs lors de l’appel de **MAPIInitialize** pour initialiser les bibliothèques MAPI et **MAPILogonEx** pour se connecter au sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="47243-108">It is important to understand the consequences of setting each of these flags when calling **MAPIInitialize** to initialize the MAPI libraries and **MAPILogonEx** to log on to the MAPI subsystem.</span></span> 
  
 <span data-ttu-id="47243-109">**Pour démarrer une session MAPI**</span><span class="sxs-lookup"><span data-stu-id="47243-109">**To start a MAPI session**</span></span>
  
1. <span data-ttu-id="47243-110">Appelez **MAPIInitialize** pour initialiser l’ensemble standard de bibliothèques MAPI.</span><span class="sxs-lookup"><span data-stu-id="47243-110">Call **MAPIInitialize** to initialize the standard set of MAPI libraries.</span></span> 
    
2. <span data-ttu-id="47243-111">Si vous devez utiliser les bibliothèques OLE, appelez la fonction [OLE OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="47243-111">If you need to use the OLE libraries, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span></span>
    
3. <span data-ttu-id="47243-112">Si vous devez utiliser la bibliothèque d’utilitaires MAPI, appelez [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="47243-112">If you need to use the MAPI utility library, call [ScInitMapiUtil](scinitmapiutil.md).</span></span>
    
4. <span data-ttu-id="47243-113">Appelez **MAPILogonEx avec** un profil valide pour vous connecter au sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="47243-113">Call **MAPILogonEx** with a valid profile to log on to the MAPI subsystem.</span></span> <span data-ttu-id="47243-114">**MAPILogonEx** vérifie la configuration de chacun des fournisseurs de services dans les services de messagerie inclus dans le profil, en inviteant l’utilisateur à fournir des informations supplémentaires si nécessaire et possible.</span><span class="sxs-lookup"><span data-stu-id="47243-114">**MAPILogonEx** verifies the configuration of each of the service providers in the message services included in the profile, prompting the user for additional information if necessary and possible.</span></span> <span data-ttu-id="47243-115">Une **fois MAPILogonEx** terminé, les fournisseurs de services configurés sont prêts pour le service.</span><span class="sxs-lookup"><span data-stu-id="47243-115">When **MAPILogonEx** completes, the configured service providers are ready for service.</span></span> 
    
## <a name="in-this-section"></a><span data-ttu-id="47243-116">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="47243-116">In this section</span></span>

[<span data-ttu-id="47243-117">Initialisation de MAPI</span><span class="sxs-lookup"><span data-stu-id="47243-117">Initializing MAPI</span></span>](initializing-mapi.md)
  
> <span data-ttu-id="47243-118">Décrit comment initialiser MAPI pour une session.</span><span class="sxs-lookup"><span data-stu-id="47243-118">Describes how to initialize MAPI for a session.</span></span>
    
[<span data-ttu-id="47243-119">Initialisation d’OLE pour MAPI</span><span class="sxs-lookup"><span data-stu-id="47243-119">Initializing OLE for MAPI</span></span>](initializing-ole-for-mapi.md)
  
> <span data-ttu-id="47243-120">Décrit les appels à effectuer pour initialiser OLE à utiliser avec MAPI.</span><span class="sxs-lookup"><span data-stu-id="47243-120">Describes the calls to make to initialize OLE for use with MAPI.</span></span>
    
[<span data-ttu-id="47243-121">Initialisation des utilitaires MAPI</span><span class="sxs-lookup"><span data-stu-id="47243-121">Initializing the MAPI Utilities</span></span>](initializing-the-mapi-utilities.md)
  
> <span data-ttu-id="47243-122">Décrit comment initialiser les utilitaires MAPI.</span><span class="sxs-lookup"><span data-stu-id="47243-122">Describes how to initialize MAPI utilities.</span></span>
    
[<span data-ttu-id="47243-123">Connexion à MAPI</span><span class="sxs-lookup"><span data-stu-id="47243-123">Logging on to MAPI</span></span>](logging-on-to-mapi.md)
  
> <span data-ttu-id="47243-124">Décrit comment les applications clientes se connectent au sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="47243-124">Describes how client applications log on to the MAPI sub system.</span></span>
    

