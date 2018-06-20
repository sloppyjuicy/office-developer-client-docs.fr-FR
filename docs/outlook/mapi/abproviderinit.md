---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 03375a11be3f6f128db5f6147c5fbe901d0a0fa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782859"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**S’applique à**: Outlook 
  
Initialise un fournisseur de carnet d’adresses pour l’opération. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Implémentée par :  <br/> |Fournisseurs de carnet d’adresses  <br/> |
|Appelée par :  <br/> |MAPI  <br/> |
   
```cpp
HRESULT ABProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPABPROVIDER FAR * lppABProvider
);
```

## <a name="parameters"></a>Paramètres

 _hInstance_
  
> [in] Instance de la bibliothèque de liens dynamiques du fournisseur de carnet d’adresses (DLL) qui MAPI utilisé lorsqu’elle est liée. 
    
 _lpMalloc_
  
> [in] Pointeur vers un objet d’allocation mémoire exposant l’interface OLE **IMalloc** . Vous devrez utiliser cette méthode de répartition lorsque vous travaillez avec certaines interfaces comme **IStream**le fournisseur de carnet d’adresses. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser lorsque MAPI pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> [in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser lorsque MAPI pour allouer plus de mémoire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser lorsque MAPI pour libérer de la mémoire. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs. Vous pouvez définir l’indicateur suivant :
    
MAPI_NT_SERVICE 
  
> Le fournisseur est chargé dans le contexte d’un service Windows, un type particulier de processus sans accès à une interface utilisateur. 
    
 _ulMAPIVer_
  
> [in] Numéro de version de l’interface de fournisseur de service (SPI) que MAPI. DLL utilise. Pour le numéro de version actuelle, consultez le MAPISPI. Fichier d’en-tête H. 
    
 _lpulProviderVer_
  
> [out] Pointeur vers le numéro de version de l’index SPI qui utilise ce fournisseur de carnet d’adresses. 
    
 _lppABProvider_
  
> [out] Pointeur vers un pointeur vers l’objet de fournisseur de carnet d’adresses initialisé.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_VERSION 
  
> La version SPI utilisée par MAPI n’est pas compatible avec le SPI utilisé par ce fournisseur.
    
## <a name="remarks"></a>Remarques

MAPI appelle la fonction de point d’entrée **ABProviderInit** d’initialisation d’un fournisseur de carnet d’adresses après une ouverture de session client. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Un fournisseur de carnet d’adresses doit implémenter **ABProviderInit** en tant que fonction d’un point d’entrée dans la DLL du fournisseur. L’implémentation doit être basée sur le prototype de fonction **ABPROVIDERINIT** , également spécifié dans MAPISPI. H. MAPI définit **ABPROVIDERINIT** pour utiliser le type appel de l’initialisation de MAPI standard, STDMAPIINITCALLTYPE, ce qui entraîne **ABProviderInit** à suivre la convention d’appel CDECL. 
  
Un fournisseur peut être initialisé plusieurs fois, à la suite d’apparaître dans plusieurs profils simultanées ou d’apparaître plusieurs fois dans le même profil. Étant donné que l’objet fournisseur contient contexte, **ABProviderInit** doit retourner un objet de fournisseur différent dans _lppABProvider_ pour chaque d’initialisation, même pour plusieurs initialisations dans le même processus. 
  
Le fournisseur de carnet d’adresses doit utiliser les fonctions désignées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart des allocation de mémoire et libération. En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel des interfaces de l’objet tels que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md). Si le fournisseur attend également utiliser l’allocation de mémoire OLE, il doit appeler la méthode **IUnknown::AddRef** de l’objet d’allocation désigné par le paramètre _lpMalloc_ . 
  
Pour plus d’informations sur l’écriture de **ABProviderInit**, voir [implémentation de fonction un Point d’entrée adresse carnet de fournisseur](implementing-an-address-book-provider-entry-point-function.md). Pour plus d’informations sur les fonctions de point d’entrée, voir [implémentation d’une fonction de Point de Service fournisseur de l’entrée](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Voir aussi

- [IABProvider : IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

