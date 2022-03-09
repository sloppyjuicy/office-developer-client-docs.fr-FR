---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
ms.openlocfilehash: 56756fecce207a99954a3ccde74e888fb14783e0
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380500"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

**S’applique à** : Outlook 2013 | Outlook 2016
  
Inscrit la fonction de préprocesseur d’un fournisseur de transport (fonction conforme au prototype [PreprocessMessage](preprocessmessage.md) ).
  
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
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur géré par la fonction de préprocesseur. Le _paramètre lpMuid_ peut être NULL.

 _lpszAdrType_
  
> [in] Pointeur vers le type d’adresse pour les messages surés par la fonction, tels que FAX, SMTP ou X500. Le _paramètre lpszAdrType_ peut être NULL.

 _lpszDLLName_
  
> [in] Pointeur vers le nom de la bibliothèque de liens dynamiques (DLL) qui contient le point d’entrée de la fonction de préprocesseur.

 _lpszPreprocess_
  
> [in] Pointeur vers le nom de la fonction de préprocesseur. Le _paramètre lpszPreprocess_ peut être NULL.

 _lpszRemovePreprocessInfo_
  
> [in] Pointeur vers le nom de la fonction qui supprime les informations de préprocesseur (fonction conforme au prototype [RemovePreprocessInfo](removepreprocessinfo.md) ). Le _paramètre lpszRemovePreprocessInfo_ peut être NULL.

 _ulFlags_
  
> Réservé ; doit être zéro.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> La fonction de préprocesseur a été enregistrée avec succès.

## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::RegisterPreprocessor** est implémentée pour les objets de prise en charge du fournisseur de transport uniquement. Les fournisseurs de transport **appellent RegisterPreprocessor** pour inscrire une fonction de préprocesseur (fonction conforme au prototype [PreprocessMessage](preprocessmessage.md) ). Une fonction de préprocesseur doit être enregistrée pour que lepooler MAPI puisse l’appeler.
  
Les paramètres _lpszPreprocess_, _lpszRemovePreprocessInfo_ et _lpszDLLName_ doivent tous pointer vers des chaînes qui peuvent être utilisées conjointement avec des appels à la fonction Win32 **GetProcAddress** , ce qui permet d’appeler correctement le point d’entrée DLL du préprocesseur.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les appels aux préprocesseurs sont spécifiques à l’ordre du fournisseur de transport. Cela signifie que si un autre fournisseur de transport devant votre fournisseur est en mesure de gérer un message, votre fonction de préprocesseur ne sera pas appelée pour ce message. Votre fonction de préprocesseur sera appelée uniquement pour les messages que vous gérerez.
  
Vous pouvez écrire des fonctions de préprocesseur pour gérer un identificateur spécifique stocké dans une structure [MAPIUID](mapiuid.md) ou un type d’adresse. Si vous spécifiez une structure **MAPIUID** dans le paramètre _lpMuid_ et un type d’adresse dans le paramètre _lpszAdrType_ , votre fonction sera appelée pour les destinataires de message qui correspondent au **MAPIUID** ou au type d’adresse. Si _lpMuid_ est NULL et _lpszAdrType_ est non NULL, votre fonction est appelée uniquement pour les destinataires dont l’adresse correspond au type pointé par _lpszAdrType_. Si _lpMuid_ est non NULL et _lpszAdrType_ est NULL, votre fonction est appelée pour les destinataires qui correspondent à **MAPIUID**, quel que soit leur type d’adresse. Si les deux sont NULL, votre fonction est appelée pour tous les destinataires du message.
  
## <a name="see-also"></a>Voir aussi

[MAPIUID](mapiuid.md)  
[PreprocessMessage](preprocessmessage.md)  
[RemovePreprocessInfo](removepreprocessinfo.md)  
[IMAPISupport : IUnknown](imapisupportiunknown.md)
