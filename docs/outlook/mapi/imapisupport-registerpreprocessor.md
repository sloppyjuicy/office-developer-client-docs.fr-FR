---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 58215de6cc4e9e68386f8f017839752acc6e1753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326564"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre la fonction de préprocesseur d'un fournisseur de transport (fonction conforme au prototype [PreprocessMessage](preprocessmessage.md) ). 
  
```cpp
HRESULT RegisterPreprocessor(
LPMAPIUID lpMuid,
LPSTR lpszAdrType,
LPSTR lpszDLLName,
LPSTR lpszPreprocess,
LPSTR lpszRemovePreprocessInfo,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpMuid_
  
> dans Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l'identificateur géré par la fonction de préprocesseur. Le paramètre _lpMuid_ peut être null. 
    
 _lpszAdrType_
  
> dans Pointeur vers le type d'adresse pour les messages sur lesquels la fonction fonctionne, comme FAX, SMTP ou X500. Le paramètre _lpszAdrType_ peut être null. 
    
 _lpszDLLName_
  
> dans Pointeur vers le nom de la bibliothèque de liens dynamiques (DLL) qui contient le point d'entrée de la fonction de préprocesseur.
    
 _lpszPreprocess_
  
> dans Pointeur vers le nom de la fonction de préprocesseur. Le paramètre _lpszPreprocess_ peut être null. 
    
 _lpszRemovePreprocessInfo_
  
> dans Pointeur vers le nom de la fonction qui supprime les informations du préprocesseur (fonction conforme au prototype [RemovePreprocessInfo](removepreprocessinfo.md) ). Le paramètre _lpszRemovePreprocessInfo_ peut être null. 
    
 _ulFlags_
  
> MSR doit être égal à zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La fonction de préprocesseur a été correctement inscrite.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: RegisterPreprocessor** est implémentée uniquement pour les objets de prise en charge du fournisseur de transport. Les fournisseurs de transport appellent **RegisterPreprocessor** pour enregistrer une fonction de préprocesseur (fonction conforme au prototype [PreprocessMessage](preprocessmessage.md) ). Une fonction de préprocesseur doit être enregistrée avant que le spouleur MAPI puisse l'appeler. 
  
Les paramètres _lpszPreprocess_, _lpszRemovePreprocessInfo_et _lpszDLLName_ doivent tous pointer vers des chaînes qui peuvent être utilisées conjointement avec des appels à la fonction **GETPROCADDRESS** Win32, ce qui permet la dll du préprocesseur. le point d'entrée doit être appelé correctement. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les appels vers des préprocesseurs sont propres à l'ordre des fournisseurs de transport. Cela signifie que si un autre fournisseur de transport devant votre fournisseur est en mesure de gérer un message, votre fonction de préprocesseur ne sera pas appelée pour ce message. Votre fonction de préprocesseur est appelée uniquement pour les messages que vous allez gérer.
  
Vous pouvez écrire des fonctions de préprocesseur pour gérer un identificateur spécifique stocké dans une structure [MAPIUID](mapiuid.md) ou un type d'adresse. Si vous spécifiez une structure **MAPIUID** dans le paramètre _lpMuid_ et un type d'adresse dans le paramètre _lpszAdrType_ , votre fonction sera appelée pour les destinataires du message qui correspondent à l' **MAPIUID** ou au type d'adresse. Si _lpMuid_ est null et _LPSZADRTYPE_ est non null, votre fonction est appelée uniquement pour les destinataires ayant une adresse correspondant au type désigné par _lpszAdrType_. Si _lpMuid_ est non null et _lpszAdrType_ est null, la fonction est appelée pour les destinataires qui correspondent à **MAPIUID**, quel que soit leur type d'adresse. Si les deux valeurs sont NULL, la fonction est appelée pour tous les destinataires du message.
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

