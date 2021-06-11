---
title: Implémentation d’un exemple d’objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a681e68c0718e49da331946d75ecb7b4fab7afe2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332829"
---
# <a name="implementing-a-sample-object"></a>Implémentation d’un exemple d’objet

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les objets de réception de notification (objets qui supportent l’interface [IMAPIAdviseSink : IUnknown)](imapiadvisesinkiunknown.md) sont des objets MAPI implémentés par les applications clientes pour le traitement des notifications. **IMAPIAdviseSink** hérite directement [d’IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) et contient une seule méthode, **OnNotify**. Par conséquent, pour implémenter un objet de sink de conseil, un client crée du code pour les trois méthodes **dans IUnknown** et [pour OnNotify](imapiadvisesink-onnotify.md).
  
Le fichier d’en-tête Mapidefs.h définit une implémentation d’interface **IMAPIAdviseSink** à l’aide DECLARE_MAPI_INTERFACE **,** comme suit :
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

Les clients qui implémentent des objets de MAPI_IMAPIADVISESINK_METHODS peuvent  définir leurs interfaces dans leurs objets manuellement ou à l’MAPI_IUNKNOWN_METHODS et **MAPI_IMAPIADVISESINK_METHODS** macros. Les implémenteurs d’objets doivent utiliser les macros d’interface chaque fois que possible pour garantir la cohérence entre les objets et pour gagner du temps et des efforts. 
  
L’implémentation des méthodes [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) et [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) est relativement simple, car en règle générale, seules quelques lignes de code sont nécessaires. Par conséquent, les clients et les fournisseurs de services qui implémentent des objets peuvent rendre leurs implémentations **AddRef** et **Release** inline. Le code suivant montre comment définir un objet de sink de conseil C++ avec des implémentations en ligne **d’AddRef** et **release**.
  
```cpp
class  CMAPIAdviseSink : public IMAPIAdviseSink
{
public:
    STDMETHODIMP QueryInterface
                    (REFIID                     riid,
                     LPVOID *                   ppvObj);
    inline STDMETHODIMP_(ULONG) AddRef
                    () { InterlockedIncrement(m_cRef);
                         ++m_cRef;
                         InterlockedDecrement(m_cRef);
                         return m_cRef; };
    inline STDMETHODIMP_(ULONG) Release
                    () { InterlockedIncrement(m_cRef);
                         ULONG ulCount = --m_cRef;
                         InterlockedDecrement(m_cRef);
                         if (!ulCount)  delete this;
                         return ulCount;};
    MAPI_IMAPIADVISESINK_METHODS(IMPL);
    BOOL WINAPI AddConnection (LPMDB pMDBObj, ULONG ulConnection);
    void WINAPI RemoveAllLinks (LPMDB pMDBObj);
// Constructors and destructors.
public :
    inline CMAPIAdviseSink  (CStoreClient * pStore)
                            { m_cRef = 1;
                              m_ulConnection = 0;
                              m_pStore = pStore;
                              AddRef;};
    ~CMAPIAdviseSink () {Release};
private :
    ULONG               m_cRef;
    CStoreClient *      m_pStore;
    ULONG               m_ulConnection;
};
 
```

En C, l’objet de sink de conseil est composé des éléments suivants :
  
- Pointeur vers un vtable qui contient des pointeurs vers les implémentations de chacune des méthodes dans **IUnknown** et **IMAPIAdviseSink**.
    
- Membres de données.
    
L’exemple de code suivant montre comment définir un objet de sink de conseil en C et construire sa vtable. 
  
```cpp
// Object definition.
typedef struct _ADVISESINK
{
    const ADVISE_Vtbl FAR *    lpVtbl;
    ULONG             cRef;
    STORECLIENT      *pStore;
    ULONG             ulConnection;
} ADVISESINK, *LPADVISESINK;
// vtable definition.
static const ADVISE_Vtbl vtblADVISE =
{
    ADVISE_QueryInterface,
    ADVISE_AddRef,
    ADVISE_Release,
    ADVISE_OnNotify
};
 
```

Après avoir déclaré un objet en C, vous devez l’initialiser en fixant le pointeur vtable sur l’adresse de la table vtable construite, comme illustré dans le code suivant :
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)
- [Mise en œuvre des objets MAPI](implementing-mapi-objects.md)

