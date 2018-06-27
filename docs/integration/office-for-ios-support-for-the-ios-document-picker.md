---
title: Prise en charge d'Office pour iOS pour le sélectionneur de document iOS
manager: soliver
ms.date: 02/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 802224ef-6eea-4929-824c-507da1c073a5
description: Office pour iOS s'intègre au sélectionneur de documents iOS par le biais de l'extension de fournisseur de documents, ce qui permet à Office d'ouvrir les fichiers stockés par un autre fournisseur de documents.
ms.openlocfilehash: 101e3cc248f994fe449a74c6c37f788fad8beed5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782513"
---
# <a name="office-for-ios-support-for-the-ios-document-picker"></a>Prise en charge d'Office pour iOS pour le sélectionneur de document iOS

Office pour iOS s'intègre au sélectionneur de documents iOS par le biais de l'extension de fournisseur de documents, ce qui permet à Office d'ouvrir les fichiers stockés par un autre fournisseur de documents.
  
Les versions de l'iOS d'Apple à compter d'iOS 8.0 incluent la [prise en charge des extensions d'application](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1). Vous pouvez utiliser ces extensions pour étendre les fonctionnalités de votre application à d'autres applications ou contextes sur le périphérique de l'utilisateur. Pour intégrer Office pour iOS au sélectionneur de documents iOS, utilisez l'[extension de fournisseur de documents](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).
  
L'extension de fournisseur de documents prend en charge quatre opérations :
  
- Importer
    
- Exporter
    
- Ouvrir
    
- Déplacer
    
Office pour iOS s'intègre à l'opération d'ouverture. Lorsque vous créez une extension de fournisseur de documents, vos utilisateurs peuvent se servir du sélectionneur de documents pour ouvrir et modifier des documents directement dans Office, sans créer une copie du fichier.
  
## <a name="learn-more-about-app-extensions-and-the-document-picker"></a>En savoir plus sur les extensions d'application et le sélectionneur de documents
<a name="bk_addresources"> </a>

- [Extensions d'application](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
    
- [Guide de programmation du sélectionneur de documents](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html)
    
- [Guide de programmation du fournisseur de documents](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
    

