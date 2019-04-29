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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: acec07df0b72685cf9ec6b21499c730b72f58c59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428283"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Initialise un fournisseur de carnets d'adresses pour l'opération. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi. h  <br/> |
|Implémenté par :  <br/> |Fournisseurs de carnets d'adresses  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |
   
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
  
> dans Instance de la bibliothèque de liens dynamiques (DLL) du fournisseur de carnet d'adresses utilisée par MAPI lors de sa liaison. 
    
 _lpMalloc_
  
> dans Pointeur vers un objet de l'allocation de mémoire qui expose **** l'interface OLE imalloc. Il se peut que le fournisseur de carnets d'adresses doive utiliser cette méthode d'allocation lorsque vous travaillez avec certaines interfaces telles que **IStream**. 
    
 _lpAllocateBuffer_
  
> dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser, le cas échéant par MAPI pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser, le cas échéant par MAPI pour allouer de la mémoire supplémentaire. 
    
 _lpFreeBuffer_
  
> dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser, le cas échéant par MAPI pour libérer de la mémoire. 
    
 _ulFlags_
  
> dans Masque de réindicateur des indicateurs. L'indicateur suivant peut être défini:
    
MAPI_NT_SERVICE 
  
> Le fournisseur est en cours de chargement dans le contexte d'un service Windows, un type spécial de processus sans accès à une interface utilisateur. 
    
 _ulMAPIVer_
  
> dans Numéro de version de l'interface du fournisseur de services (SPI) MAPI. DLL utilise. Pour le numéro de version actuel, consultez le MAPISPI. Fichier d'en-tête H. 
    
 _lpulProviderVer_
  
> remarquer Pointeur vers le numéro de version du SPI que ce fournisseur de carnet d'adresses utilise. 
    
 _lppABProvider_
  
> remarquer Pointeur vers un pointeur vers l'objet fournisseur de carnet d'adresses initialisé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_VERSION 
  
> La version SPI utilisée par MAPI n'est pas compatible avec le SPI utilisé par ce fournisseur.
    
## <a name="remarks"></a>Remarques

MAPI appelle la fonction de point d'entrée **ABProviderInit** pour initialiser un fournisseur de carnets d'adresses à la suite d'une ouverture de session client. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Un fournisseur de carnets d'adresses doit implémenter **ABProviderInit** en tant que fonction de point d'entrée dans la dll du fournisseur. L'implémentation doit être basée sur le prototype de fonction **ABPROVIDERINIT** , également spécifié dans MAPISPI. H. MAPI définit **ABPROVIDERINIT** pour utiliser le type d'appel d'initialisation MAPI standard, STDMAPIINITCALLTYPE, qui force **ABPROVIDERINIT** à suivre la Convention d'appel CDECL. 
  
Un fournisseur peut être initialisé plusieurs fois, en raison de son affichage simultané dans plusieurs profils, ou de plusieurs fois dans le même profil. Étant donné que l'objet fournisseur contient le contexte, **ABProviderInit** doit renvoyer un objet fournisseur différent dans _lppABProvider_ pour chaque initialisation, même pour plusieurs initialisations dans le même processus. 
  
Le fournisseur de carnets d'adresses doit utiliser les fonctions pointées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart de l'allocation et de la libération de mémoire. En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire à utiliser par les applications clientes lors de l'appel d'interfaces d'objets telles que [IMAPIProp:: GetProps](imapiprop-getprops.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md). Si le fournisseur s'attend également à utiliser l'allocateur de mémoire OLE, il doit appeler la méthode **IUnknown:: AddRef** de l'objet allocater pointé par le paramètre _lpMalloc_ . 
  
Pour plus d'informations sur l'écriture de **ABProviderInit**, consultez la rubrique [implémentation d'une fonction de point d'entrée de fournisseur de carnet d'adresses](implementing-an-address-book-provider-entry-point-function.md). Pour plus d'informations sur les fonctions de point d'entrée, consultez [la rubrique implémentation d'une fonction de point d'entrée du fournisseur de services](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Voir aussi

- [IABProvider : IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

