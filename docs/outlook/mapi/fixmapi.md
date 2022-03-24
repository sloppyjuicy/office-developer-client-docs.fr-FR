---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: Effectue une copie de sauvegarde de la copie actuelle de mapi32.dll sur l’ordinateur client et restaure les mapi32.dll avec la bibliothèque stub MAPI, mapistub.dll.
ms.openlocfilehash: c305c295adf63ed43337c820d20cc7075572b971
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762269"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue une copie de sauvegarde de la copie actuelle de mapi32.dll sur l’ordinateur client et restaure les mapi32.dll avec la bibliothèque stub MAPI, mapistub.dll.
  
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

Si la fonction réussit, la valeur de retour est une valeur non nulle.
  
Si la fonction échoue, la valeur de retour est zéro. Pour obtenir des informations d’erreur étendues, appelez la fonction Du Kit de développement logiciel (SDK) microsoft Windows, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Remarques

 **FixMAPI ne** remplace pas le fichier mapi32.dll si le fichier est marqué comme étant en lecture seule. 
  
 **FixMAPI ne** remplace pas le mapi32.dll si Microsoft Exchange Server est installé sur l’ordinateur. 
  
Lorsque **FixMAPI** effectue une copie de sauvegarde de la copie actuelle de mapi32.dll sur l’ordinateur, il attribue à la copie de sauvegarde un nom différent de « mapi32.dll ». Il dirige ensuite les appels ultérieurs destinés à cet assembly vers la copie de sauvegarde. 
  
## <a name="see-also"></a>Voir aussi



[KB 256946 : vous recevez un message d’erreur de conflit de programme lorsque vous Outlook 2000](https://support.microsoft.com/kb/256946)
  
[KB 228457 : Description de l’outil Fixmapi.exe inclus dans Internet Explorer 5](https://support.microsoft.com/kb/228457)

