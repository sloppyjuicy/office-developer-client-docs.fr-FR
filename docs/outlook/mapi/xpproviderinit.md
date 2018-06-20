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
ms.openlocfilehash: 0415e782a98102314ce732f744c0d29590f646c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787491"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**S’applique à**: Outlook 
  
Initialise un fournisseur de transport pour l’opération.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Implémentée par :  <br/> |Fournisseurs de transport  <br/> |
|Appelée par :  <br/> |MAPI  <br/> |
   
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
  
> [in] Instance de la bibliothèque de liens dynamiques du fournisseur de transport (DLL) qui MAPI utilisé lors de son chargement de la DLL.
    
 _lpMalloc_
  
> [in] Pointeur vers un objet d’allocation mémoire exposant l’interface OLE **IMalloc** . Le fournisseur de transport devrez peut-être utiliser cette méthode de répartition lorsque vous travaillez avec certaines interfaces comme **IStream**. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> [in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer plus de mémoire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs. Vous pouvez définir l’indicateur suivant :
    
MAPI_NT_SERVICE 
  
> Le fournisseur est chargé dans le contexte d’un service Windows, un type particulier de processus sans accès à une interface utilisateur. 
    
 _ulMAPIVer_
  
> [in] Numéro de version de l’interface de fournisseur de service (SPI) qui utilise Mapi.dll. Pour le numéro de version actuelle, consultez le fichier d’en-tête Mapispi.h. 
    
 _lpulProviderVer_
  
> [out] Pointeur vers le numéro de version de l’index SPI qui utilise ce fournisseur de transport. 
    
 _lppXPProvider_
  
> [out] Pointeur vers un pointeur vers l’objet de fournisseur de transport initialisé.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_VERSION 
  
> La version SPI utilisée par MAPI n’est pas compatible avec le SPI utilisé par ce fournisseur.
    
## <a name="remarks"></a>Remarques

MAPI appelle la fonction de point d’entrée **XPProviderInit** d’initialisation d’un fournisseur de transport après une ouverture de session client. **XPProviderInit** est appelée une seule fois pour chaque fournisseur de transport spécifié dans le profil du client. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Un fournisseur de transport doit implémenter **XPProviderInit** en tant que fonction d’un point d’entrée dans la DLL du fournisseur. L’implémentation doit être basée sur le prototype de fonction **XPPROVIDERINIT** , également spécifié dans Mapispi.h. MAPI définit **XPPROVIDERINIT** pour utiliser le type appel de l’initialisation de MAPI standard, STDMAPIINITCALLTYPE, ce qui entraîne **XPProviderInit** à suivre la convention d’appel CDECL. L’avantage de CDECL est que les appels peuvent être tentés, même si le nombre de paramètres d’appel ne correspond pas au nombre de paramètres définis. 
  
Un fournisseur peut être initialisé plusieurs fois à la suite d’apparaître dans plusieurs profils simultanées ou d’apparaître plusieurs fois dans le même profil. Étant donné que l’objet fournisseur contient contexte, **XPProviderInit** doit retourner un objet de fournisseur différent dans _lppXPProvider_ pour chaque d’initialisation, même pour plusieurs initialisations dans le même processus. 
  
Le fournisseur de transport doit utiliser les fonctions désignées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart des allocation de mémoire et libération. En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel des interfaces de l’objet tels que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md). Si le fournisseur attend également utiliser l’allocation de mémoire OLE, il doit appeler la méthode **IUnknown::AddRef** de l’objet d’allocation désigné par le paramètre _lpMalloc_ . 
  
Pour plus d’informations sur l’écriture de **XPProviderInit**, voir [l’initialisation du fournisseur de Transport](initializing-the-transport-provider.md). Pour plus d’informations sur les fonctions de point d’entrée, voir [implémentation d’une fonction de Point de Service fournisseur de l’entrée](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Voir aussi



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

