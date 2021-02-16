---
title: Prise en charge d'Office pour Android pour la structure d'accès au stockage Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: Office pour Android s'intègre à la structure d'accès au stockage Android, permettant à Office d'ouvrir les fichiers stockés par un autre fournisseur de documents.
ms.openlocfilehash: 24d7e48106aeb5e58a668b94cbde00eaa9175230
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300349"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a><span data-ttu-id="0703c-103">Prise en charge d'Office pour Android pour la structure d'accès au stockage Android</span><span class="sxs-lookup"><span data-stu-id="0703c-103">Office for Android support for the Android Storage Access Framework</span></span>

<span data-ttu-id="0703c-104">Office pour Android s'intègre à la structure d'accès au stockage Android, permettant à Office d'ouvrir les fichiers stockés par un autre fournisseur de documents.</span><span class="sxs-lookup"><span data-stu-id="0703c-104">Office for Android integrates with the Android Storage Access Framework, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="0703c-p101">Android 4.4 (API niveau 19) présente la structure d'accès au stockage (Storage Access Framework - SAF). La structure SAF permet aux utilisateurs de parcourir et d'ouvrir des documents, des images et d'autres fichiers parmi tous leurs fournisseurs de stockage de documents préférés. Une interface utilisateur standard permet aux utilisateurs de parcourir les fichiers et d'y accéder de manière cohérente parmi les applications et les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="0703c-p101">Android 4.4 (API level 19) introduces the Storage Access Framework (SAF). The SAF enables users to browse and open documents, images, and other files across all their preferred document storage providers. A standard UI lets users browse files and access them in a consistent way across apps and providers.</span></span>
  
## <a name="implement-a-document-provider"></a><span data-ttu-id="0703c-108">Mise en œuvre d'un fournisseur de documents</span><span class="sxs-lookup"><span data-stu-id="0703c-108">Implement a document provider</span></span>

<span data-ttu-id="0703c-p102">Si vous développez une application qui fournit des services de stockage de documents, vous pouvez mettre vos fichiers à disposition via la structure SAF en [écrivant à un fournisseur de documents personnalisé](https://developer.android.com/guide/topics/providers/document-provider.html). Les applications Office peuvent ensuite appeler l'intention [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) et/ou [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) pour recevoir les fichiers renvoyés par votre fournisseur de documents. Notez que cette intention peut inclure des filtres qui permettront d'affiner ensuite les critères.</span><span class="sxs-lookup"><span data-stu-id="0703c-p102">If you're developing an app that provides storage services for documents, you can make your files available through the SAF by [writing a custom document provider](https://developer.android.com/guide/topics/providers/document-provider.html). Office apps can then invoke the [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) and/or [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) intent to receive the files returned by your document provider. Note that the intent might include filters to further refine the criteria.</span></span> 
  
## <a name="enable-free-consumer-edits"></a><span data-ttu-id="0703c-112">Activation des modifications gratuites</span><span class="sxs-lookup"><span data-stu-id="0703c-112">Enable free consumer edits</span></span>

<span data-ttu-id="0703c-p103">Les utilisateurs peuvent se connecter aux applications Office avec un compte Microsoft gratuit pour créer ou modifier des documents qui sont enregistrés dans un service de stockage axé sur le consommateur. Le tableau suivant répertorie les propriétés obligatoires que les fournisseurs doivent fournir dans le cadre de ce dispositif pour permettre aux utilisateurs de modifier gratuitement les documents disponibles via la structure Storage Access Framework.</span><span class="sxs-lookup"><span data-stu-id="0703c-p103">Users can sign in to the Office apps with a free Microsoft account to create or edit docs that are stored in a consumer-oriented storage service. The following table lists the mandatory properties that providers must supply as part of the cursor, to enable free consumer edit for documents accessed via the Storage Access Framework.</span></span>
  
|<span data-ttu-id="0703c-115">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="0703c-115">**Property**</span></span>|<span data-ttu-id="0703c-116">**Index**</span><span class="sxs-lookup"><span data-stu-id="0703c-116">**Index**</span></span>|<span data-ttu-id="0703c-117">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="0703c-117">**Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0703c-118">Type de document</span><span class="sxs-lookup"><span data-stu-id="0703c-118">Document Type</span></span>  <br/> |<span data-ttu-id="0703c-119">com_microsoft_office_doctype</span><span class="sxs-lookup"><span data-stu-id="0703c-119">com_microsoft_office_doctype</span></span>  <br/> |<span data-ttu-id="0703c-120">\<consumer\></span><span class="sxs-lookup"><span data-stu-id="0703c-120">\<consumer\></span></span>  <br/> |
|<span data-ttu-id="0703c-121">Pseudonyme du service</span><span class="sxs-lookup"><span data-stu-id="0703c-121">Service Friendly Name</span></span>  <br/> |<span data-ttu-id="0703c-122">com_microsoft_office_servicename</span><span class="sxs-lookup"><span data-stu-id="0703c-122">com_microsoft_office_servicename</span></span>  <br/> |<span data-ttu-id="0703c-p104">Tout pseudonyme du service utilisé pour identifier un document dans la liste des derniers fichiers utilisés des applications Office. Notez que la propriété « Conditions d'utilisation » doit être fournie avant le pseudonyme pour pouvoir afficher le service.</span><span class="sxs-lookup"><span data-stu-id="0703c-p104">Any user-friendly name for the service, used to identify a document in the Recent list in the Office apps. Note that the "Terms of Use Agreement" property must be supplied before the friendly name for the service can be displayed.</span></span>  <br/> |
|<span data-ttu-id="0703c-125">Conditions d'utilisation</span><span class="sxs-lookup"><span data-stu-id="0703c-125">Terms of Use Agreement</span></span>  <br/> |<span data-ttu-id="0703c-126">com_microsoft_office_termsofuse</span><span class="sxs-lookup"><span data-stu-id="0703c-126">com_microsoft_office_termsofuse</span></span>  <br/> |<span data-ttu-id="0703c-127">\<J’accepte les termes du contrat disponible à l’adresse https://go.microsoft.com/fwlink/p/?LinkId=528381\></span><span class="sxs-lookup"><span data-stu-id="0703c-127">\<I agree to the terms located at https://go.microsoft.com/fwlink/p/?LinkId=528381\></span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0703c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0703c-128">See also</span></span>
<span data-ttu-id="0703c-129"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="0703c-129"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="0703c-130">Intégration à Office</span><span class="sxs-lookup"><span data-stu-id="0703c-130">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="0703c-131">Conditions de base du fournisseur de contenu</span><span class="sxs-lookup"><span data-stu-id="0703c-131">Content Provider Basics</span></span>](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [<span data-ttu-id="0703c-132">Création d'un fournisseur de contenu</span><span class="sxs-lookup"><span data-stu-id="0703c-132">Creating a Content Provider</span></span>](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [<span data-ttu-id="0703c-133">Guide du développeur de la structure Storage Access Framework</span><span class="sxs-lookup"><span data-stu-id="0703c-133">Storage Access Framework Developer Guide</span></span>](https://developer.android.com/guide/topics/providers/document-provider.html)
    

