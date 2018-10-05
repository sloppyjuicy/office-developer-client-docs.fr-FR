---
title: Exigences techniques
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: Cette rubrique décrit les langages de programmation pris en charge, la méthode et la visibilité COM renvoient des exigences de type et les détails de l’extensibilité de fournisseur Outlook Social Connector (OSC) DLL.
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383113"
---
# <a name="technical-requirements"></a><span data-ttu-id="9bf1c-103">Exigences techniques</span><span class="sxs-lookup"><span data-stu-id="9bf1c-103">Technical requirements</span></span>

<span data-ttu-id="9bf1c-104">Cette rubrique décrit les langages de programmation pris en charge, la méthode et la visibilité COM renvoient des exigences de type et les détails de l’extensibilité de fournisseur Outlook Social Connector (OSC) DLL.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="9bf1c-105">Langage de programmation en matière de COM</span><span class="sxs-lookup"><span data-stu-id="9bf1c-105">Programming language and COM requirements</span></span>

<span data-ttu-id="9bf1c-106">Vous pouvez créer un fournisseur OSC à l’aide des langages managés tels que Visual c# ou Visual Basic ou langages non managés tels que Visual C++.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="9bf1c-107">Vous pouvez utiliser n’importe quel outil que vous pouvez créer un composant DLL COM visibles pour développer un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="9bf1c-108">La décision d’utiliser un langage managé ou non managé pour développer un fournisseur doit prendre en compte la taille de téléchargement et les dépendances du package d’installation fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="9bf1c-109">Un fournisseur OSC doit être visible par COM, tel que défini par les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9bf1c-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="9bf1c-110">Après l’installation, un fournisseur OSC doit être enregistré à l’aide de l’inscription automatique COM ou regsvr32.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="9bf1c-111">Un enregistrement d’un fournisseur OSC DLL COM enregistre le fournisseur dans HKCU ou HKLM.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="9bf1c-112">ProgID d’un fournisseur est enregistré sous `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="9bf1c-113">Un fournisseur OSC développé dans un langage managé est visible par COM.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="9bf1c-114">Un fournisseur OSC doit ajouter les valeurs dans le Registre Windows qui indiquent que la DLL du fournisseur prend en charge un seul thread cloisonné et apartment multithread (MTA) modèles de thread.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="9bf1c-115">Pour plus d’informations sur les modèles de thread COM, voir [Descriptions et fonctionnement de OLE modèles de thread](https://support.microsoft.com/kb/150777).</span><span class="sxs-lookup"><span data-stu-id="9bf1c-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="9bf1c-116">Méthodes de l’extensibilité de fournisseur OSC doivent retourner types primitifs comme **chaîne** ou **bool**.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="9bf1c-117">Certains **chaîne** renvoie les valeurs doivent être conformes à la définition de schéma pour l’extensibilité de fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="9bf1c-118">XML uniquement est pris en charge en tant que valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="9bf1c-119">Détails de l’extensibilité de fournisseur OSC DLL</span><span class="sxs-lookup"><span data-stu-id="9bf1c-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="9bf1c-120">Le composant qui prend en charge l’extensibilité de fournisseur OSC est l’extensibilité du fournisseur OSC DLL.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="9bf1c-121">Les développeurs tiers peuvent créer des DLL de fournisseur OSC à l’aide de ces interfaces d’extensibilité.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="9bf1c-122">La liste suivante présente les détails de l’extensibilité de fournisseur OSC DLL :</span><span class="sxs-lookup"><span data-stu-id="9bf1c-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="9bf1c-123">Nom du fichier DLL extensibilité : socialprovider.dll</span><span class="sxs-lookup"><span data-stu-id="9bf1c-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="9bf1c-124">Nom convivial de la DLL de l’extensibilité : extensibilité de fournisseur Social Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="9bf1c-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="9bf1c-125">Version principale de l’extensibilité DLL : 15.0</span><span class="sxs-lookup"><span data-stu-id="9bf1c-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="9bf1c-126">Version de bibliothèque de types de DLL Extensibiilty : 1.1</span><span class="sxs-lookup"><span data-stu-id="9bf1c-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="9bf1c-127">Informations techniques diverses</span><span class="sxs-lookup"><span data-stu-id="9bf1c-127">Miscellaneous technical information</span></span>

<span data-ttu-id="9bf1c-128">JavaScript Object Notation (JSON) n’est pas pris en charge dans le modèle d’extensibilité de fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="9bf1c-129">Il n’existe aucune dépendance sur un analyseur XML.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="9bf1c-130">Le fournisseur OSC permettre utiliser un analyseur XML qui est inclus avec Office, telles que Microsoft XML Core Services (MSXML), utilisez le code XML l’analyse des fonctionnalités intégrées à Microsoft .NET Framework ou un analyseur XML de tiers.</span><span class="sxs-lookup"><span data-stu-id="9bf1c-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9bf1c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bf1c-131">See also</span></span>

- [<span data-ttu-id="9bf1c-132">Meilleures pratiques pour le développement d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="9bf1c-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="9bf1c-133">Étapes rapides pour apprendre à développer un fournisseur</span><span class="sxs-lookup"><span data-stu-id="9bf1c-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="9bf1c-134">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="9bf1c-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="9bf1c-135">Prise en main du développement d'un fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="9bf1c-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

