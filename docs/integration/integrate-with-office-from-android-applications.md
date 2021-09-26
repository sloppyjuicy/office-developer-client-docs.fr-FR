---
title: Intégration à Office à partir d'applications Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a765fa49-a272-4047-9147-59cc68e5dd27
description: Office pour Android fournit une solution extensible qui permet l'intégration avec des applications tierces. Vous pouvez exécuter une intégration avec Office à partir de votre application Android en transférant les utilisateurs de votre application vers Office.
ms.openlocfilehash: c5a2be61b767a27d4ebe0ee1fa2eb22a2b2801da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631250"
---
# <a name="integrate-with-office-from-android-applications"></a>Intégration à Office à partir d'applications Android

Office pour Android fournit une solution extensible qui permet l'intégration avec des applications tierces. Vous pouvez exécuter une intégration avec Office à partir de votre application Android en transférant les utilisateurs de votre application vers Office.
  
Vous pouvez permettre aux utilisateurs qui exécutent Office sur un appareil Android d'ouvrir et de modifier les fichiers stockés dans SharePoint ou OneDrive à partir de n'importe quelle application. Pour ce faire, transférez les fichiers vers Office par l'intermédiaire de gestionnaires de protocole et assurez-vous qu'Office est invoqué de manière à ce qu'Office puisse comprendre.
  
Une fois le fichier édité par l'utilisateur, ce dernier peut appuyer sur la touche de retour de l'appareil pour revenir à l'application de stockage d'origine.
  
## <a name="verify-that-office-has-been-installed"></a>Assurez-vous qu'Office est bien installé

Votre application référente doit d'abord vérifier qu'une application Office particulière est installée. Les applications Office suivantes peuvent être installées sur des périphériques Android pour l'affichage et la modification de documents : 
  
- Excel
    
- PowerPoint
    
- Word
    
Utilisez Android PackageManager pour déterminer si une application Office spécifique est installée sur l'appareil. Le tableau suivant répertorie les noms des paquets pour les applications Office que vous pouvez utiliser dans ce processus.
  
|**Application**|**Nom du paquet**|
|:-----|:-----|
|Excel  <br/> |com.microsoft.office.excel  <br/> |
|PowerPoint  <br/> |com.microsoft.office.powerpoint  <br/> |
|Word  <br/> |com.microsoft.office.word  <br/> |
   
### <a name="prompt-the-user-to-install-office"></a>Inviter l'utilisateur à installer Office

Si une application Office spécifique n'est pas installée, vous pouvez inviter l'utilisateur à l'installer. Le tableau suivant répertorie les emplacements d'installation disponibles pour les applications Office.
  
|**Application**|**Google Play Store**|
|:-----|:-----|
|Excel  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.excel](https://play.google.com/store/apps/details?id=com.microsoft.office.excel) <br/> |
|PowerPoint  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint](https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint) <br/> |
|Word  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.word](https://play.google.com/store/apps/details?id=com.microsoft.office.word) <br/> |
   
## <a name="invoke-office"></a>Appeler Office

Lorsque l'application Office est installée, votre application référente peut appeler Office en transmettant les détails suivants :
  
- Protocole Office
    
- Mode d'ouverture
    
- URL
    
Format de schéma :
  
 `<Office protocol><open mode>|u|<URL>`
  
L'exemple suivant montre une demande d'appel de fichier Word pour modification :
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx`
  
### <a name="office-protocols"></a>Protocoles Office

Le tableau suivant répertorie les protocoles pour chaque application Office.
  
|**Application**|**Protocole**|
|:-----|:-----|
|Excel  <br/> |ms-excel:  <br/> |
|PowerPoint  <br/> |ms-powerpoint:  <br/> |
|Word  <br/> |ms-word:  <br/> |
   
### <a name="open-mode"></a>Mode d'ouverture

Les applications Office peuvent ouvrir les fichiers directement en mode d'affichage (ofv) ou de modification (ofe), ce dernier étant le mode par défaut.
  
Format de schéma :
  
 `<ofv or ofe>`
  
### <a name="url"></a>URL

L'URL comprend trois parties :
  
- Déclaration indiquant que le fichier est ouvert pour modification (ofe)
    
- Descripteur de l'URL (|u|)
    
- URL
    
L'URL doit être codée et il doit s'agir d'un lien direct vers le fichier (et non d'une redirection). Si le format de l'URL ne peut pas être géré par Office ou en cas d'échec du téléchargement, Office ne renvoie pas l'utilisateur vers l'application appelante.
  
Format de schéma :
  
 `|u|<document URL>`
  
## <a name="see-also"></a>Voir aussi
<a name="bk_addresources"> </a>

- [Intégration à Office](integrate-with-office.md)
    
- [PackageManager](https://developer.android.com/reference/android/content/pm/PackageManager.html)
    
- [GetPackageManager()](https://developer.android.com/reference/android/content/Context.html)
    

