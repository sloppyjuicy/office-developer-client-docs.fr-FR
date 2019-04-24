---
title: Exigences techniques
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: Cette rubrique décrit les langages de programmation pris en charge, la visibilité COM et les conditions requises pour le type de retour de la méthode, ainsi que les détails de la DLL d'extensibilité du fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329154"
---
# <a name="technical-requirements"></a><span data-ttu-id="987f1-103">Exigences techniques</span><span class="sxs-lookup"><span data-stu-id="987f1-103">Technical requirements</span></span>

<span data-ttu-id="987f1-104">Cette rubrique décrit les langages de programmation pris en charge, la visibilité COM et les conditions requises pour le type de retour de la méthode, ainsi que les détails de la DLL d'extensibilité du fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="987f1-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="987f1-105">Configuration requise pour le langage de programmation et COM</span><span class="sxs-lookup"><span data-stu-id="987f1-105">Programming language and COM requirements</span></span>

<span data-ttu-id="987f1-106">Vous pouvez créer un fournisseur OSC en utilisant des langages managés, tels que Visual C# ou Visual Basic, ou des langages non managés, tels que Visual C++.</span><span class="sxs-lookup"><span data-stu-id="987f1-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="987f1-107">Vous pouvez utiliser n'importe quel outil capable de créer un composant DLL visible par COM pour développer un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="987f1-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="987f1-108">La décision d'utiliser un langage managé ou non managé pour développer un fournisseur doit prendre en compte la taille de téléchargement et les dépendances du package d'installation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="987f1-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="987f1-109">Un fournisseur OSC doit être visible par COM, comme défini par les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="987f1-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="987f1-110">Après l'installation, un fournisseur OSC doit être enregistré à l'aide de l'auto-enregistrement COM ou de regsvr32.</span><span class="sxs-lookup"><span data-stu-id="987f1-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="987f1-111">L'inscription COM d'une DLL de fournisseur OSC inscrit le fournisseur sous HKCU ou HKLM.</span><span class="sxs-lookup"><span data-stu-id="987f1-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="987f1-112">Le ProgID d'un fournisseur est enregistré `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`sous.</span><span class="sxs-lookup"><span data-stu-id="987f1-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="987f1-113">Un fournisseur OSC développé dans un langage managé est visible par COM.</span><span class="sxs-lookup"><span data-stu-id="987f1-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="987f1-114">Un fournisseur OSC doit ajouter des valeurs au registre Windows qui indiquent que la DLL du fournisseur prend en charge les modèles de thread cloisonné (STA) et multithread (MTA).</span><span class="sxs-lookup"><span data-stu-id="987f1-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="987f1-115">Pour plus d'informations sur les modèles de thread COM, voir [descriptions and workings of OLE threadIng Models](https://support.microsoft.com/kb/150777).</span><span class="sxs-lookup"><span data-stu-id="987f1-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="987f1-116">Les méthodes de l'extensibilité du fournisseur OSC doivent retourner des types primitifs, tels que **String** ou **bool**.</span><span class="sxs-lookup"><span data-stu-id="987f1-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="987f1-117">Certaines valeurs de retour de **chaîne** doivent être conformes à la définition de schéma pour l'extensibilité du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="987f1-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="987f1-118">Seul XML est pris en charge en tant que valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="987f1-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="987f1-119">Détails de la DLL d'extensibilité du fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="987f1-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="987f1-120">Le composant qui prend en charge l'extensibilité du fournisseur OSC est la DLL d'extensibilité du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="987f1-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="987f1-121">Les développeurs tiers peuvent créer des dll de fournisseur OSC à l'aide de ces interfaces d'extensibilité.</span><span class="sxs-lookup"><span data-stu-id="987f1-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="987f1-122">La liste suivante indique les détails de la DLL d'extensibilité du fournisseur OSC:</span><span class="sxs-lookup"><span data-stu-id="987f1-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="987f1-123">Nom du fichier DLL d'extensibilité: socialprovider. dll</span><span class="sxs-lookup"><span data-stu-id="987f1-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="987f1-124">Nom convivial de la DLL d'extensibilité: extensibilité des fournisseurs de réseaux sociaux Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="987f1-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="987f1-125">Version principale de la DLL d'extensibilité: 15,0</span><span class="sxs-lookup"><span data-stu-id="987f1-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="987f1-126">Extensibiilty DLL TypeLib version: 1,1</span><span class="sxs-lookup"><span data-stu-id="987f1-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="987f1-127">Informations techniques diverses</span><span class="sxs-lookup"><span data-stu-id="987f1-127">Miscellaneous technical information</span></span>

<span data-ttu-id="987f1-128">JavaScript Object Notation (JSON) n'est pas pris en charge dans le modèle d'extensibilité du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="987f1-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="987f1-129">Il n'existe aucune dépendance vis-à-vis d'un analyseur XML.</span><span class="sxs-lookup"><span data-stu-id="987f1-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="987f1-130">Le fournisseur OSC peut utiliser un analyseur XML inclus dans Office, comme Microsoft XML Core Services (MSXML), utiliser les fonctionnalités d'analyse XML intégrées à Microsoft .NET Framework ou utiliser un analyseur XML tiers.</span><span class="sxs-lookup"><span data-stu-id="987f1-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="987f1-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="987f1-131">See also</span></span>

- [<span data-ttu-id="987f1-132">Meilleures pratiques pour le développement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="987f1-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="987f1-133">Étapes rapides pour apprendre à développer un fournisseur</span><span class="sxs-lookup"><span data-stu-id="987f1-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="987f1-134">Déploiement d'un fournisseur</span><span class="sxs-lookup"><span data-stu-id="987f1-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="987f1-135">Prise en main du développement d'un fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="987f1-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

