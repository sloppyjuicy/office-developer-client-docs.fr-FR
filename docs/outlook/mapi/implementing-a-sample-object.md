---
title: L’implémentation d’un exemple d’objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 85de8dd7211fa19b7cdbda9f5ced1f00a736ca9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784159"
---
# <a name="implementing-a-sample-object"></a>L’implémentation d’un exemple d’objet

**S’applique à**: Outlook 
  
Objets de récepteur de notification — les objets qui prennent en charge la [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface — sont des objets MAPI que les applications clientes implémentent pour traiter les notifications. **IMAPIAdviseSink** hérite directement de [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) et contient une seule méthode, **OnNotify**. Par conséquent, pour implémenter un objet de récepteur advise, un client crée du code pour les trois méthodes de **IUnknown** et [OnNotify](imapiadvisesink-onnotify.md).
  
Le fichier d’en-tête Mapidefs.h définit une implémentation d’interface **IMAPIAdviseSink** à l’aide de **DECLARE_MAPI_INTERFACE**, comme suit :
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

Clients qui implémentent des objets récepteurs peuvent définir leurs interfaces dans leurs objets manuellement ou avec les macros **MAPI_IUNKNOWN_METHODS** et **MAPI_IMAPIADVISESINK_METHODS** de notification. L’implémentation d’objet doit utiliser les macros d’interface chaque fois que possible pour assurer la cohérence entre les objets et de gagner du temps. 
  
Implémentez les méthodes [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) and [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) est relativement simple, car il est généralement uniquement quelques lignes de code sont nécessaires. Par conséquent, les clients et les fournisseurs de services qui implémentent des objets peut-il leur inline implémentations **AddRef** et **Release** . Le code suivant montre comment définir un C++ conseiller objet récepteur avec des implémentations inline **AddRef** et **Release**.
  
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

Dans C, l’objet de récepteur advise est composée des éléments suivants :
  
- Pointeur vers un vtable qui contient des pointeurs vers des implémentations de chacune des méthodes dans **IUnknown** et **IMAPIAdviseSink**.
    
- Membres de données.
    
L’exemple de code suivant montre comment définir l’objet récepteur advise dans C et construire ses vtable. 
  
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

Une fois que vous déclarez un objet C, vous devez l’initialiser en définissant le pointeur vtable à l’adresse de la vtable construite, comme indiqué dans le code suivant :
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble de la propri�t� MAPI](mapi-property-overview.md)
- [Implémentation d’objets MAPI](implementing-mapi-objects.md)

