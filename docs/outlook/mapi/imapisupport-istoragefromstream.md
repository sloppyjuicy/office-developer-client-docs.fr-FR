---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a73c87f172b4c97379bb9cd117679d3947c188af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783999"
---
# <a name="imapisupportistoragefromstream"></a>IMAPISupport::IStorageFromStream

  
  
**S’applique à**: Outlook 
  
Implémente un objet de stockage pour accéder à un objet stream.
  
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au flux désigné par _lpUnkIn_. Une des valeurs suivantes sont valide : IID_IStream, IID_ILockBytes, ou **valeur null**, ce qui indique que l’interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) doit être utilisé pour accéder au flux. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet de stockage doit être créé par rapport à l’objet stream. Par défaut, le stockage est créé avec un accès en lecture seule et le flux démarre à la position zéro dans le stockage. Les indicateurs suivants peuvent être définis :
    
STGSTRM_CREATE 
  
> Un nouvel objet de stockage doit être créé pour l’objet stream.
    
STGSTRM_CURRENT 
  
> L’objet de stockage doit commencer à la position actuelle du flux.
    
STGSTRM_MODIFY 
  
> L’appelant doit avoir l’autorisation de lecture/écriture à l’objet de stockage renvoyé.
    
STGSTRM_RESET 
  
> L’objet de stockage doit commencer à la position zéro.
    
 _lppStorageOut_
  
> [out] Pointeur vers un pointeur vers l’objet de stockage.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’objet de stockage a été créé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::IStorageFromStream** est implémentée pour tous les objets de prise en charge de fournisseur de service. Fournisseurs de services d’appel **IStorageFromStream** pour créer un objet de stockage à utiliser pour ouvrir les propriétés. Fournisseurs de services qui ont leur propre implémentation de l’interface [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) est inutile d’appeler **IStorageFromStream**. 
  
L’objet de stockage créé par **IStorageFromStream** appelle la méthode du flux [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) pour incrémenter son décompte de références, puis le décrémente le décompte lorsque l’utilisateur relâche le stockage. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Lorsque la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de l’un de vos objets est appelée à le pour ouverture d’une propriété avec l’interface **IStorage** , effectuez les tâches suivantes : 
  
1. Ouvrir un objet stream avec l’autorisation de lecture/écriture de la propriété.
    
2. En interne, sélectionnez le flux de propriétés en tant qu’un objet de stockage.
    
3. Appelez **IStorageFromStream** pour générer un objet de stockage. 
    
4. Retourne un pointeur vers cet objet de stockage.
    
Si vous implémentez des interfaces supplémentaires qui utilisent l’objet de stockage, créez un objet qui encapsule l’objet de stockage et implémenter un méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) de niveau supérieur. 
  
Ne pas autoriser une propriété à ouvrir avec l’interface **IStream** si elle a été créée avec **IStorage**. Inversement, ne pas autoriser une propriété à ouvrir avec l’interface **IStorage** si elle a été créée avec **IStream**. 
  
Avec une exception, il est possible d’utiliser l’interface **IStreamDocfile** pour l’acheminement d’un objet de stockage d’un conteneur à un autre, mais l’identificateur d’interface IID_IStreamDocfile doit être transmis dans _de la méthode **OpenProperty** lpInterface _paramètre. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

