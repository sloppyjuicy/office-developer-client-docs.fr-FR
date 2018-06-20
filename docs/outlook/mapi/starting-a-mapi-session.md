---
title: Démarrage d’une Session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d683d5fc959b219569417c74494cb47d7c2c059e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787246"
---
# <a name="starting-a-mapi-session"></a><span data-ttu-id="b4dd8-103">Démarrage d’une Session MAPI</span><span class="sxs-lookup"><span data-stu-id="b4dd8-103">Starting a MAPI Session</span></span>

  
  
<span data-ttu-id="b4dd8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4dd8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4dd8-105">Bien qu’il existe une quantité importante de travail effectué au cours de la session de démarrage, les tâches requises sont minimes.</span><span class="sxs-lookup"><span data-stu-id="b4dd8-105">Although there is a significant amount of work performed during session start up, the required tasks are minimal.</span></span> <span data-ttu-id="b4dd8-106">Cette opération est effectuée dans l’interface MAPI de traitement des appels [exécuter MAPIInitialize](mapiinitialize.md) et [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="b4dd8-106">Much of this work is done in the MAPI processing of the [MAPIInitialize](mapiinitialize.md) and [MAPILogonEx](mapilogonex.md) calls.</span></span> <span data-ttu-id="b4dd8-107">Ces deux fonctions acceptent des indicateurs en tant que paramètres d’entrée pour contrôler des aspects de la session de gestion de la notification et l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b4dd8-107">Both of these functions accept flags as input parameters for controlling aspects of the session such as notification handling and the user interface.</span></span> <span data-ttu-id="b4dd8-108">Il est important de comprendre les conséquences de la définition de chacune de ces indicateurs lors de l’appel **exécuter MAPIInitialize** pour initialiser les bibliothèques MAPI et **MAPILogonEx** pour ouvrir une session sur le sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="b4dd8-108">It is important to understand the consequences of setting each of these flags when calling **MAPIInitialize** to initialize the MAPI libraries and **MAPILogonEx** to log on to the MAPI subsystem.</span></span> 
  
 <span data-ttu-id="b4dd8-109">**Pour démarrer une session MAPI**</span><span class="sxs-lookup"><span data-stu-id="b4dd8-109">**To start a MAPI session**</span></span>
  
1. <span data-ttu-id="b4dd8-110">Appelez **exécuter MAPIInitialize** pour initialiser l’ensemble standard de bibliothèques de MAPI.</span><span class="sxs-lookup"><span data-stu-id="b4dd8-110">Call **MAPIInitialize** to initialize the standard set of MAPI libraries.</span></span> 
    
2. <span data-ttu-id="b4dd8-111">Si vous devez utiliser les bibliothèques OLE, appelez la fonction OLE [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b4dd8-111">If you need to use the OLE libraries, call the OLE function [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span></span>
    
3. <span data-ttu-id="b4dd8-112">Si vous devez utiliser la bibliothèque d’utilitaires MAPI, appelez [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="b4dd8-112">If you need to use the MAPI utility library, call [ScInitMapiUtil](scinitmapiutil.md).</span></span>
    
4. <span data-ttu-id="b4dd8-113">Appelle **MAPILogonEx** avec un profil valide pour ouvrir une session sur le sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="b4dd8-113">Call **MAPILogonEx** with a valid profile to log on to the MAPI subsystem.</span></span> <span data-ttu-id="b4dd8-114">**MAPILogonEx** vérifie la configuration de chacun des fournisseurs de services dans les services de message inclus dans le profil, inviter l’utilisateur pour plus d’informations si nécessaire et possible.</span><span class="sxs-lookup"><span data-stu-id="b4dd8-114">**MAPILogonEx** verifies the configuration of each of the service providers in the message services included in the profile, prompting the user for additional information if necessary and possible.</span></span> <span data-ttu-id="b4dd8-115">Lorsque **MAPILogonEx** est terminée, les fournisseurs de service configuré sont prêts pour le service.</span><span class="sxs-lookup"><span data-stu-id="b4dd8-115">When **MAPILogonEx** completes, the configured service providers are ready for service.</span></span> 
    
## <a name="in-this-section"></a><span data-ttu-id="b4dd8-116">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b4dd8-116">In this section</span></span>

[<span data-ttu-id="b4dd8-117">L’initialisation de MAPI</span><span class="sxs-lookup"><span data-stu-id="b4dd8-117">Initializing MAPI</span></span>](initializing-mapi.md)
  
> <span data-ttu-id="b4dd8-118">Décrit comment initialiser MAPI pour une session.</span><span class="sxs-lookup"><span data-stu-id="b4dd8-118">Describes how to initialize MAPI for a session.</span></span>
    
[<span data-ttu-id="b4dd8-119">L’initialisation d’OLE pour MAPI</span><span class="sxs-lookup"><span data-stu-id="b4dd8-119">Initializing OLE for MAPI</span></span>](initializing-ole-for-mapi.md)
  
> <span data-ttu-id="b4dd8-120">Décrit les appels s’initialiser OLE pour une utilisation avec MAPI.</span><span class="sxs-lookup"><span data-stu-id="b4dd8-120">Describes the calls to make to initialize OLE for use with MAPI.</span></span>
    
[<span data-ttu-id="b4dd8-121">Initialisation des utilitaires MAPI</span><span class="sxs-lookup"><span data-stu-id="b4dd8-121">Initializing the MAPI Utilities</span></span>](initializing-the-mapi-utilities.md)
  
> <span data-ttu-id="b4dd8-122">Décrit comment initialiser les utilitaires MAPI.</span><span class="sxs-lookup"><span data-stu-id="b4dd8-122">Describes how to initialize MAPI utilities.</span></span>
    
[<span data-ttu-id="b4dd8-123">Se connecter à MAPI</span><span class="sxs-lookup"><span data-stu-id="b4dd8-123">Logging on to MAPI</span></span>](logging-on-to-mapi.md)
  
> <span data-ttu-id="b4dd8-124">Décrit comment les applications clientes se connecter au système sub MAPI.</span><span class="sxs-lookup"><span data-stu-id="b4dd8-124">Describes how client applications log on to the MAPI sub system.</span></span>
    

