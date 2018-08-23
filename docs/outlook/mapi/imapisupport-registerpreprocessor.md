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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 87f5e3f159542359f614a6ab698e6f06a2faf41a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567915"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Enregistre la fonction préprocesseur d’un fournisseur de transport (une fonction qui est conforme au prototype [PreprocessMessage](preprocessmessage.md) ). 
  
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
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur qui gère la fonction préprocesseur. Le paramètre _lpMuid_ peut être NULL. 
    
 _lpszAdrType_
  
> [in] Un pointeur vers le type d’adresse pour les messages de la fonction fonctionne, telles que télécopie, SMTP ou X500. Le paramètre _lpszAdrType_ peut être NULL. 
    
 _lpszDLLName_
  
> [in] Pointeur vers le nom de la bibliothèque de liens dynamiques (DLL) qui contient le point d’entrée de la fonction préprocesseur.
    
 _lpszPreprocess_
  
> [in] Pointeur vers le nom de la fonction préprocesseur. Le paramètre _lpszPreprocess_ peut être NULL. 
    
 _lpszRemovePreprocessInfo_
  
> [in] Pointeur vers le nom de la fonction qui supprime les informations du préprocesseur (une fonction qui est conforme au prototype [RemovePreprocessInfo](removepreprocessinfo.md) ). Le paramètre _lpszRemovePreprocessInfo_ peut être NULL. 
    
 _ulFlags_
  
> Réservé ; doit être égal à zéro.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La fonction préprocesseur a été enregistrée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::RegisterPreprocessor** est implémentée pour les objets de prise en charge des fournisseur de transport uniquement. Fournisseurs de transport appellent **RegisterPreprocessor** pour enregistrer une fonction préprocesseur (une fonction qui est conforme au prototype [PreprocessMessage](preprocessmessage.md) ). Une fonction préprocesseur doit être enregistrée avant le spouleur MAPI permettre appeler. 
  
Les paramètres _lpszPreprocess_, _lpszRemovePreprocessInfo_et _lpszDLLName_ doivent tous pointer les chaînes qui peuvent être utilisées conjointement avec les appels à la fonction Win32 **GetProcAddress** , ce qui permet DLL du préprocesseur point d’entrée appelé correctement. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Les appels vers Préprocesseurs sont spécifiques à l’ordre des fournisseurs de transport. Cela signifie que si un autre fournisseur de transport à votre fournisseur est en mesure de gérer un message, votre fonction préprocesseur ne sera pas appelée pour ce message. Votre fonction préprocesseur être appelée uniquement pour les messages que vous allez gérer.
  
Vous pouvez écrire des fonctions préprocesseur pour gérer un identificateur spécifique que stocké dans une structure [MAPIUID](mapiuid.md) ou un type d’adresse. Si vous spécifiez à la fois une structure **MAPIUID** dans le paramètre _lpMuid_ et un type d’adresse dans le paramètre _lpszAdrType_ , votre fonction sera appelée pour les destinataires du message qui correspondent à la **MAPIUID** ou le type d’adresse. Si _lpMuid_ a la valeur NULL et _lpszAdrType_ n’est pas NULL, votre fonction sera appelée uniquement pour les destinataires auxquels une adresse qui correspond au type désigné par _lpszAdrType_. Si _lpMuid_ n’est pas NULL et _lpszAdrType_ est NULL, votre fonction sera appelée pour des destinataires qui correspondent à **MAPIUID**, quel que soit leur type d’adresse. Si les deux sont NULL, la fonction est appelée pour tous les destinataires du message.
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

