---
title: XPProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.XPProviderInit
api_type:
- COM
ms.assetid: df6eacf4-1cf9-4c25-806f-f87c38dad597
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325654"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Initialise un fournisseur de transport pour l'opération.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi. h  <br/> |
|Implémenté par :  <br/> |Fournisseurs de transport  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |
   
```cpp
HRESULT XPProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPXPPROVIDER FAR * lppXPProvider
);
```

## <a name="parameters"></a>Paramètres

 _hInstance_
  
> dans Instance de la bibliothèque de liens dynamiques (DLL) du fournisseur de transport utilisée par MAPI lors de la chargement de la DLL.
    
 _lpMalloc_
  
> dans Pointeur vers un objet de l'allocation de mémoire qui expose **** l'interface OLE imalloc. Le fournisseur de transport peut avoir besoin d'utiliser cette méthode d'allocation lorsque vous travaillez avec certaines interfaces telles que **IStream**. 
    
 _lpAllocateBuffer_
  
> dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire. 
    
 _lpFreeBuffer_
  
> dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire. 
    
 _ulFlags_
  
> dans Masque de réindicateur des indicateurs. L'indicateur suivant peut être défini:
    
MAPI_NT_SERVICE 
  
> Le fournisseur est en cours de chargement dans le contexte d'un service Windows, un type spécial de processus sans accès à une interface utilisateur. 
    
 _ulMAPIVer_
  
> dans Numéro de version de l'interface du fournisseur de services (SPI) utilisée par MAPI. dll. Pour le numéro de version actuel, consultez le fichier d'en-tête Mapispi. h. 
    
 _lpulProviderVer_
  
> remarquer Pointeur vers le numéro de version du SPI utilisé par ce fournisseur de transport. 
    
 _lppXPProvider_
  
> remarquer Pointeur vers un pointeur vers l'objet fournisseur de transport initialisé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_VERSION 
  
> La version SPI utilisée par MAPI n'est pas compatible avec le SPI utilisé par ce fournisseur.
    
## <a name="remarks"></a>Remarques

MAPI appelle la fonction de point d'entrée **XPProviderInit** pour initialiser un fournisseur de transport à la suite d'une ouverture de session client. **XPProviderInit** est appelé une fois pour chaque fournisseur de transport spécifié dans le profil du client. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Un fournisseur de transport doit implémenter **XPProviderInit** en tant que fonction de point d'entrée dans la dll du fournisseur. L'implémentation doit être basée sur le prototype de fonction **XPPROVIDERINIT** , également spécifié dans Mapispi. h. MAPI définit **XPPROVIDERINIT** pour utiliser le type d'appel d'initialisation MAPI standard, STDMAPIINITCALLTYPE, qui force **XPPROVIDERINIT** à suivre la Convention d'appel CDECL. L'un des avantages de CDECL est que les appels peuvent être tentés même si le nombre de paramètres d'appel ne correspond pas au nombre de paramètres définis. 
  
Un fournisseur peut être initialisé plusieurs fois à la suite de l'affichage simultané de plusieurs profils ou de plusieurs fois dans le même profil. Étant donné que l'objet fournisseur contient le contexte, **XPProviderInit** doit renvoyer un objet fournisseur différent dans _lppXPProvider_ pour chaque initialisation, même pour plusieurs initialisations dans le même processus. 
  
Le fournisseur de transport doit utiliser les fonctions pointées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart de l'allocation et de la libération de mémoire. En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire à utiliser par les applications clientes lors de l'appel d'interfaces d'objets telles que [IMAPIProp:: GetProps](imapiprop-getprops.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md). Si le fournisseur s'attend également à utiliser l'allocateur de mémoire OLE, il doit appeler la méthode **IUnknown:: AddRef** de l'objet allocater pointé par le paramètre _lpMalloc_ . 
  
Pour plus d'informations sur l'écriture de **XPProviderInit**, consultez [la rubrique initialisation du fournisseur de transport](initializing-the-transport-provider.md). Pour plus d'informations sur les fonctions de point d'entrée, consultez [la rubrique implémentation d'une fonction de point d'entrée du fournisseur de services](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Voir aussi



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

