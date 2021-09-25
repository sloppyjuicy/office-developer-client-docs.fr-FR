---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 04cce495a0149b77429467eb814c5b7a6960dd2f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575847"
---
# <a name="imapisupportistoragefromstream"></a>IMAPISupport::IStorageFromStream

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Implémente un objet de stockage pour accéder à un flux.
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>Paramètres

 _lpUnkIn_
  
> [in] Pointeur vers un objet stream.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au flux pointé par  _lpUnkIn_. L’une des valeurs suivantes est valide : IID_IStream, IID_ILockBytes ou **null,** ce qui indique que l’interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) doit être utilisée pour accéder au flux. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet de stockage doit être créé par rapport à l’objet de flux. Par défaut, le stockage est créé avec un accès en lecture seule et le flux démarre à la position zéro dans le stockage. Les indicateurs suivants peuvent être définies :
    
STGSTRM_CREATE 
  
> Un nouvel objet de stockage doit être créé pour l’objet de flux.
    
STGSTRM_CURRENT 
  
> L’objet de stockage doit commencer à la position actuelle du flux.
    
STGSTRM_MODIFY 
  
> L’appelant doit avoir une autorisation de lecture/écriture sur l’objet de stockage renvoyé.
    
STGSTRM_RESET 
  
> L’objet de stockage doit commencer à la position zéro.
    
 _lppStorageOut_
  
> [out] Pointeur vers un pointeur vers l’objet de stockage.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’objet de stockage a été créé avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::IStorageFromStream** est implémentée pour tous les objets de prise en charge du fournisseur de services. Les fournisseurs de services **appellent IStorageFromStream** pour créer un objet de stockage à utiliser pour ouvrir des propriétés particulières. Les fournisseurs de services qui ont leur propre implémentation de l’interface [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) n’ont pas besoin d’appeler **IStorageFromStream**. 
  
L’objet de stockage créé par **IStorageFromStream** appelle la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) du flux pour incrémenter son nombre de références, puis décrémente le nombre lorsque le stockage est libéré. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque la [méthode IMAPIProp::OpenProperty](imapiprop-openproperty.md) de l’un de vos objets est appelée pour ouvrir une propriété avec l’interface **IStorage,** effectuez les tâches suivantes : 
  
1. Ouvrez un objet de flux avec une autorisation de lecture/écriture pour la propriété.
    
2. Marquez en interne le flux de propriété en tant qu’objet de stockage.
    
3. Appelez **IStorageFromStream** pour générer un objet de stockage. 
    
4. Renvoyer un pointeur vers cet objet de stockage.
    
Si vous implémentez des interfaces supplémentaires qui utilisent l’objet de stockage, créez un objet qui enveloppe l’objet de stockage et implémentez une méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) de niveau supérieur. 
  
N’autorisez pas l’ouverture d’une propriété avec l’interface **IStream** si elle a été créée avec **IStorage**. Inversement, n’autorisez pas l’ouverture d’une propriété avec l’interface **IStorage** si elle a été créée avec **IStream**. 
  
À une exception près, il est acceptable d’utiliser l’interface **IStreamDocfile** pour diffuser un objet de stockage d’un conteneur à un autre, mais l’identificateur d’interface IID_IStreamDocfile doit être transmis dans le paramètre _lpInterface_ de la méthode **OpenProperty.** 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

