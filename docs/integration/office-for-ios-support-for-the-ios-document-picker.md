---
title: Prise en charge d'Office pour iOS pour le sélectionneur de document iOS
manager: soliver
ms.date: 02/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 802224ef-6eea-4929-824c-507da1c073a5
description: Office pour iOS s'intègre au sélectionneur de documents iOS par le biais de l'extension de fournisseur de documents, ce qui permet à Office d'ouvrir les fichiers stockés par un autre fournisseur de documents.
ms.openlocfilehash: e3a3374c7fd33bb00ed076075eb6199c24eec923
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410664"
---
# <a name="office-for-ios-support-for-the-ios-document-picker"></a><span data-ttu-id="0f3dc-103">Prise en charge d'Office pour iOS pour le sélectionneur de document iOS</span><span class="sxs-lookup"><span data-stu-id="0f3dc-103">Office for iOS support for the iOS Document Picker</span></span>

<span data-ttu-id="0f3dc-104">Office pour iOS s'intègre au sélectionneur de documents iOS par le biais de l'extension de fournisseur de documents, ce qui permet à Office d'ouvrir les fichiers stockés par un autre fournisseur de documents.</span><span class="sxs-lookup"><span data-stu-id="0f3dc-104">Office for iOS integrates with the iOS Document Picker by means of the Document Provider extension, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="0f3dc-p101">Les versions de l'iOS d'Apple à compter d'iOS 8.0 incluent la [prise en charge des extensions d'application](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1). Vous pouvez utiliser ces extensions pour étendre les fonctionnalités de votre application à d'autres applications ou contextes sur le périphérique de l'utilisateur. Pour intégrer Office pour iOS au sélectionneur de documents iOS, utilisez l'[extension de fournisseur de documents](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).</span><span class="sxs-lookup"><span data-stu-id="0f3dc-p101">Versions of the Apple iOS starting with iOS 8.0 include [app extension support](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1). You can use these extensions to expand the functionality of your application into other apps or contexts on the user's device. To integrate Office for iOS with the iOS Document Picker, you use the [Document Provider extension](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).</span></span>
  
<span data-ttu-id="0f3dc-108">L'extension de fournisseur de documents prend en charge quatre opérations :</span><span class="sxs-lookup"><span data-stu-id="0f3dc-108">The Document Provider extension supports four operations:</span></span>
  
- <span data-ttu-id="0f3dc-109">Importer</span><span class="sxs-lookup"><span data-stu-id="0f3dc-109">Import</span></span>
    
- <span data-ttu-id="0f3dc-110">Exporter</span><span class="sxs-lookup"><span data-stu-id="0f3dc-110">Export</span></span>
    
- <span data-ttu-id="0f3dc-111">Ouvrir</span><span class="sxs-lookup"><span data-stu-id="0f3dc-111">Open</span></span>
    
- <span data-ttu-id="0f3dc-112">Déplacer</span><span class="sxs-lookup"><span data-stu-id="0f3dc-112">Move</span></span>
    
<span data-ttu-id="0f3dc-p102">Office pour iOS s'intègre à l'opération d'ouverture. Lorsque vous créez une extension de fournisseur de documents, vos utilisateurs peuvent se servir du sélectionneur de documents pour ouvrir et modifier des documents directement dans Office, sans créer une copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="0f3dc-p102">Office for iOS integrates with the open operation. When you create a Document Provider extension, your users can use the Document Picker to open and edit documents directly in Office without creating a duplicate copy of the file.</span></span>
  
## <a name="learn-more-about-app-extensions-and-the-document-picker"></a><span data-ttu-id="0f3dc-115">En savoir plus sur les extensions d'application et le sélectionneur de documents</span><span class="sxs-lookup"><span data-stu-id="0f3dc-115">Learn more about app extensions and the Document Picker</span></span>
<span data-ttu-id="0f3dc-116"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="0f3dc-116"></span></span>

- [<span data-ttu-id="0f3dc-117">Extensions d'application</span><span class="sxs-lookup"><span data-stu-id="0f3dc-117">App extensions</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
    
- [<span data-ttu-id="0f3dc-118">Guide de programmation du sélectionneur de documents</span><span class="sxs-lookup"><span data-stu-id="0f3dc-118">Document Picker Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html)
    
- [<span data-ttu-id="0f3dc-119">Guide de programmation du fournisseur de documents</span><span class="sxs-lookup"><span data-stu-id="0f3dc-119">Document Provider Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
    

