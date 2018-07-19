---
title: Prise en charge d'Office pour Android pour la structure d'accès au stockage Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: Office pour Android s'intègre à la structure d'accès au stockage Android, permettant à Office d'ouvrir les fichiers stockés par un autre fournisseur de documents.
ms.openlocfilehash: c217eb2aa6c0974c32e60f5015449de7b157d39d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782517"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a>Prise en charge d'Office pour Android pour la structure d'accès au stockage Android

Office pour Android s'intègre à la structure d'accès au stockage Android, permettant à Office d'ouvrir les fichiers stockés par un autre fournisseur de documents.
  
Android 4.4 (API niveau 19) présente la structure d'accès au stockage (Storage Access Framework - SAF). La structure SAF permet aux utilisateurs de parcourir et d'ouvrir des documents, des images et d'autres fichiers parmi tous leurs fournisseurs de stockage de documents préférés. Une interface utilisateur standard permet aux utilisateurs de parcourir les fichiers et d'y accéder de manière cohérente parmi les applications et les fournisseurs.
  
## <a name="implement-a-document-provider"></a>Mise en œuvre d'un fournisseur de documents

Si vous développez une application qui fournit des services de stockage de documents, vous pouvez mettre vos fichiers à disposition via la structure SAF en [écrivant à un fournisseur de documents personnalisé](https://developer.android.com/guide/topics/providers/document-provider.html). Les applications Office peuvent ensuite appeler l'intention [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) et/ou [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) pour recevoir les fichiers renvoyés par votre fournisseur de documents. Notez que cette intention peut inclure des filtres qui permettront d'affiner ensuite les critères. 
  
## <a name="enable-free-consumer-edits"></a>Activation des modifications gratuites

Les utilisateurs peuvent se connecter aux applications Office avec un compte Microsoft gratuit pour créer ou modifier des documents qui sont enregistrés dans un service de stockage axé sur le consommateur. Le tableau suivant répertorie les propriétés obligatoires que les fournisseurs doivent fournir dans le cadre de ce dispositif pour permettre aux utilisateurs de modifier gratuitement les documents disponibles via la structure Storage Access Framework.
  
|**Propriété**|**Index**|**Valeur**|
|:-----|:-----|:-----|
|Type de document  <br/> |com_microsoft_office_doctype  <br/> |\<consumer\>  <br/> |
|Pseudonyme du service  <br/> |com_microsoft_office_servicename  <br/> |Tout pseudonyme du service utilisé pour identifier un document dans la liste des derniers fichiers utilisés des applications Office. Notez que la propriété « Conditions d'utilisation » doit être fournie avant le pseudonyme pour pouvoir afficher le service.  <br/> |
|Conditions d'utilisation  <br/> |com_microsoft_office_termsofuse  <br/> |\<J’accepte les termes du contrat disponible à l’adresse http://go.microsoft.com/fwlink/p/?LinkId=528381\>  <br/> |
   
## <a name="see-also"></a>Voir aussi
<a name="bk_addresources"> </a>

- [Intégration à Office](integrate-with-office.md)
    
- [Conditions de base du fournisseur de contenu](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [Création d'un fournisseur de contenu](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [Guide du développeur de la structure Storage Access Framework](https://developer.android.com/guide/topics/providers/document-provider.html)
    

