---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334960"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue une copie de sauvegarde de la copie actuelle de Mapi32. dll sur l'ordinateur client et restaure Mapi32. dll à l'aide de la bibliothèque de stubs MAPI, mapistub. dll.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exporté par:  <br/> |mapistub. dll  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Valeurs de retour

Si la fonction réussit, la valeur renvoyée est une valeur non nulle.
  
Si la fonction échoue, la valeur renvoyée est zéro. Pour obtenir des informations détaillées sur les erreurs, appelez la fonction de kit de développement logiciel (SDK) de Microsoft Windows, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Remarques

 **Fixmapi** ne remplace pas le fichier Mapi32. dll actuel si le fichier est marqué en lecture seule. 
  
 **Fixmapi** ne remplace pas le fichier Mapi32. dll actuel si Microsoft Exchange Server est installé sur l'ordinateur. 
  
Lorsque **Fixmapi** crée une copie de sauvegarde de la copie actuelle de Mapi32. dll sur l'ordinateur, il affecte à la copie de sauvegarde un nom différent de «Mapi32. dll». Il dirige ensuite les appels suivants destinés à cet assembly vers la copie de sauvegarde. 
  
## <a name="see-also"></a>Voir aussi



[KB 256946: vous recevez un message d'erreur de conflit de programmes lorsque vous démarrez Outlook 2000](https://support.microsoft.com/kb/256946)
  
[KB 228457: description de l'outil Fixmapi. exe inclus dans Internet Explorer 5](https://support.microsoft.com/kb/228457)

