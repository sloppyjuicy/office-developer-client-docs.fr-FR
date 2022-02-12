---
title: Prise en charge d'Office pour Android pour la structure d'accès au stockage Android
manager: lindalu
ms.date: 02/09/2022
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: Office pour Android s'intègre à la structure d'accès au stockage Android, permettant à Office d'ouvrir les fichiers stockés par un autre fournisseur de documents.
ms.openlocfilehash: fa548134d5b5b38620514d63ed347228c24486ce
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774971"
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
|Type de document  |com_microsoft_office_doctype  |\<consumer\>  |
|Pseudonyme du service  |com_microsoft_office_servicename tout nom convivial pour le service, utilisé pour identifier un document dans la liste Récents dans les applications Office client. Notez que la propriété « Conditions d'utilisation » doit être fournie avant le pseudonyme pour pouvoir afficher le service. |
|Conditions d'utilisation  <br/> |com_microsoft_office_termsofuse |\<I agree to the terms located at https://go.microsoft.com/fwlink/p/?LinkId=528381\>  |
   
## <a name="see-also"></a>Voir aussi

- [Intégration à Office](integrate-with-office.md)    
- [Conditions de base du fournisseur de contenu](https://developer.android.com/guide/topics/providers/content-provider-basics.html)    
- [Création d'un fournisseur de contenu](https://developer.android.com/guide/topics/providers/content-provider-creating.html)    
- [Guide du développeur de la structure Storage Access Framework](https://developer.android.com/guide/topics/providers/document-provider.html)
