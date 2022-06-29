---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: Effectue une copie de sauvegarde de la copie actuelle de mapi32.dll sur l’ordinateur client et restaure mapi32.dll avec la bibliothèque de stub MAPI, mapistub.dll.
ms.openlocfilehash: 60dbf11daf25fe3263345b0a3c863033d9094547
ms.sourcegitcommit: 1da753936975e64349cbd6954cf1c1732289a0b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2022
ms.locfileid: "66448440"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue une copie de sauvegarde de la copie actuelle de mapi32.dll sur l’ordinateur client et restaure mapi32.dll avec la bibliothèque de stub MAPI, mapistub.dll.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Exporté par :  <br/> |mapistub.dll  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Valeurs de retour

Si la fonction réussit, la valeur de retour est une valeur différente de zéro.
  
Si la fonction échoue, la valeur de retour est zéro. Pour obtenir des informations sur les erreurs étendues, appelez la fonction du Kit de développement logiciel (SDK) Microsoft Windows, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Remarques

 **FixMAPI** ne remplace pas le fichier mapi32.dll actuel si le fichier est marqué comme étant en lecture seule. 
  
 **FixMAPI** ne remplace pas le mapi32.dll actuel si Microsoft Exchange Server est installé sur l’ordinateur. 
  
Quand **FixMAPI** effectue une copie de sauvegarde de la copie actuelle de mapi32.dll sur l’ordinateur, il affecte à la copie de sauvegarde un nom différent de « mapi32.dll ». Il dirige ensuite les appels suivants destinés à cet assembly vers la copie de sauvegarde. 
  
## <a name="see-also"></a>Voir aussi



<!-- [KB 256946: You receive a program conflict error message when you start Outlook 2000](https://support.microsoft.com/kb/256946)
  
[KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5](https://support.microsoft.com/kb/228457) -->

