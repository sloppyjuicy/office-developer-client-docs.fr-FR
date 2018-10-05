---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383813"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une copie de sauvegarde de la copie en cours de mapi32.dll sur le client ordinateur et restaure mapi32.dll avec la bibliothèque stub MAPI, mapistub.dll.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exportés par :  <br/> |Mapistub.dll  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Valeurs de retour

Si la fonction réussit, la valeur de retour est une valeur non nulle.
  
Si la fonction échoue, la valeur de retour est égale à zéro. Pour obtenir des informations d’erreur étendues, appelez la fonction du Kit de développement logiciel (SDK) de Microsoft Windows, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Remarques

 **FixMAPI** ne remplace pas le fichier mapi32.dll en cours si le fichier est marqué comme étant en lecture seule. 
  
 **FixMAPI** ne remplace pas le fichier mapi32.dll en cours si Microsoft Exchange Server est installé sur l’ordinateur. 
  
**FixMAPI** lorsqu’une copie de sauvegarde de la copie en cours de mapi32.dll sur l’ordinateur, elle affecte à la copie de sauvegarde un nom différent de « mapi32.dll ». Puis dirige les appels suivants destinés à cet assembly à la copie de sauvegarde. 
  
## <a name="see-also"></a>Voir aussi



[KB 256946 : Vous recevez un message d’erreur de conflit programme lorsque vous démarrez Outlook 2000](https://support.microsoft.com/kb/256946)
  
[KB 228457 : Description de l’outil Fixmapi.exe inclus avec Internet Explorer 5](https://support.microsoft.com/kb/228457)

