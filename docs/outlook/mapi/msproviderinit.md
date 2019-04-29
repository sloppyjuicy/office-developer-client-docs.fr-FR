---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9a5f8b44f9d795282ccfd61fd32a306c5478ed21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416236"
---
# <a name="msproviderinit"></a>MSProviderInit

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Initialise un fournisseur de banque de messages pour l'opération.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi. h  <br/> |
|Implémenté par :  <br/> |Fournisseurs de banques de messages  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |
   
```cpp
HRESULT MSProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPMSPROVIDER FAR * lppMSProvider
);
```

## <a name="parameters"></a>Paramètres

 _hInstance_
  
> dans Instance de la bibliothèque de liens dynamiques (DLL) du fournisseur de banque de messages utilisée par MAPI lors de sa liaison. 
    
 _lpMalloc_
  
> dans Pointeur vers un objet de l'allocation de mémoire qui expose **** l'interface OLE imalloc. Il se peut que le fournisseur de banque de messages doive utiliser cette méthode d'allocation lorsque vous travaillez avec certaines interfaces telles que **IStream**. 
    
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
  
> dans Numéro de version de l'interface du fournisseur de services (SPI) utilisée par MAPI. Pour le numéro de version actuel, consultez le fichier d'en-tête Mapispi. h. 
    
 _lpulProviderVer_
  
> remarquer Pointeur vers le numéro de version du SPI que ce fournisseur de banque de messages utilise. 
    
 _lppMSProvider_
  
> remarquer Pointeur vers un pointeur vers l'objet fournisseur de banque de messages initialisée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_VERSION 
  
> La version SPI utilisée par MAPI n'est pas compatible avec le SPI utilisé par ce fournisseur.
    
## <a name="remarks"></a>Remarques

MAPI appelle la fonction de point d'entrée **MSProviderInit** pour initialiser un fournisseur de banque de messages à la suite d'une ouverture de session client. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Un fournisseur de banque de messages doit implémenter **MSProviderInit** comme fonction de point d'entrée dans la dll du fournisseur. L'implémentation doit être basée sur le prototype de fonction **MSPROVIDERINIT** , également spécifié dans MAPISPI. H. MAPI définit **MSPROVIDERINIT** pour utiliser le type d'appel d'initialisation MAPI standard, STDMAPIINITCALLTYPE, qui force **MSPROVIDERINIT** à suivre la Convention d'appel CDECL. L'un des avantages de CDECL est que les appels peuvent être tentés même si le nombre de paramètres d'appel ne correspond pas au nombre de paramètres définis. 
  
Un fournisseur peut être initialisé plusieurs fois, en raison de son affichage simultané dans plusieurs profils, ou de plusieurs fois dans le même profil. Étant donné que l'objet fournisseur contient le contexte, **MSProviderInit** doit renvoyer un objet fournisseur différent dans _lppMSProvider_ pour chaque initialisation, même pour plusieurs initialisations dans le même processus. 
  
La DLL du fournisseur ne doit pas être liée à mapix. dll. Au lieu de cela, il doit utiliser ces pointeurs pour l'allocation ou la désallocation de la mémoire. 
  
Le fournisseur de banque de messages doit utiliser les fonctions pointées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart de l'allocation et de la libération de mémoire. En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire à utiliser par les applications clientes lors de l'appel d'interfaces d'objets telles que [IMAPIProp:: GetProps](imapiprop-getprops.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md). Si le fournisseur s'attend également à utiliser l'allocateur de mémoire OLE, il doit appeler la méthode **IUnknown:: AddRef** de l'objet allocater pointé par le paramètre _lpMalloc_ . 
  
Pour plus d'informations sur l'écriture de **MSProviderInit**, voir [chargement des fournisseurs de banques de messages](loading-message-store-providers.md). Pour plus d'informations sur les fonctions de point d'entrée, consultez [la rubrique implémentation d'une fonction de point d'entrée du fournisseur de services](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Voir aussi



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

