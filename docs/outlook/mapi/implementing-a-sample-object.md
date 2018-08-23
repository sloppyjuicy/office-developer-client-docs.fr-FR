---
title: L’implémentation d’un exemple d’objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7d2f5fc2f26019902b27750613f7c360a751cd51
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582930"
---
# <a name="implementing-a-sample-object"></a><span data-ttu-id="0c647-103">L’implémentation d’un exemple d’objet</span><span class="sxs-lookup"><span data-stu-id="0c647-103">Implementing a sample object</span></span>

<span data-ttu-id="0c647-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c647-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c647-105">Objets de récepteur de notification — les objets qui prennent en charge la [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface — sont des objets MAPI que les applications clientes implémentent pour traiter les notifications.</span><span class="sxs-lookup"><span data-stu-id="0c647-105">Advise sink objects — objects that support the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface — are MAPI objects that client applications implement for processing notifications.</span></span> <span data-ttu-id="0c647-106">**IMAPIAdviseSink** hérite directement de [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) et contient une seule méthode, **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="0c647-106">**IMAPIAdviseSink** inherits directly from [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) and contains only one method, **OnNotify**.</span></span> <span data-ttu-id="0c647-107">Par conséquent, pour implémenter un objet de récepteur advise, un client crée du code pour les trois méthodes de **IUnknown** et [OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="0c647-107">Therefore, to implement an advise sink object, a client creates code for the three methods in **IUnknown** and for [OnNotify](imapiadvisesink-onnotify.md).</span></span>
  
<span data-ttu-id="0c647-108">Le fichier d’en-tête Mapidefs.h définit une implémentation d’interface **IMAPIAdviseSink** à l’aide de **DECLARE_MAPI_INTERFACE**, comme suit :</span><span class="sxs-lookup"><span data-stu-id="0c647-108">The Mapidefs.h header file defines an **IMAPIAdviseSink** interface implementation by using **DECLARE_MAPI_INTERFACE**, as follows:</span></span>
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

<span data-ttu-id="0c647-109">Clients qui implémentent des objets récepteurs peuvent définir leurs interfaces dans leurs objets manuellement ou avec les macros **MAPI_IUNKNOWN_METHODS** et **MAPI_IMAPIADVISESINK_METHODS** de notification.</span><span class="sxs-lookup"><span data-stu-id="0c647-109">Clients that implement advise sink objects can define their interfaces in their objects manually or with the **MAPI_IUNKNOWN_METHODS** and **MAPI_IMAPIADVISESINK_METHODS** macros.</span></span> <span data-ttu-id="0c647-110">L’implémentation d’objet doit utiliser les macros d’interface chaque fois que possible pour assurer la cohérence entre les objets et de gagner du temps.</span><span class="sxs-lookup"><span data-stu-id="0c647-110">Object implementers should use the interface macros whenever possible to ensure consistency across objects and to save time and effort.</span></span> 
  
<span data-ttu-id="0c647-111">Implémentez les méthodes [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) and [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) est relativement simple, car il est généralement uniquement quelques lignes de code sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0c647-111">Implementing the [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) and [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) methods is relatively simple because typically only a few lines of code are needed.</span></span> <span data-ttu-id="0c647-112">Par conséquent, les clients et les fournisseurs de services qui implémentent des objets peut-il leur inline implémentations **AddRef** et **Release** .</span><span class="sxs-lookup"><span data-stu-id="0c647-112">Therefore, clients and service providers that implement objects can make their **AddRef** and **Release** implementations inline.</span></span> <span data-ttu-id="0c647-113">Le code suivant montre comment définir un C++ conseiller objet récepteur avec des implémentations inline **AddRef** et **Release**.</span><span class="sxs-lookup"><span data-stu-id="0c647-113">The following code shows how to define a C++ advise sink object with inline implementations of **AddRef** and **Release**.</span></span>
  
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

<span data-ttu-id="0c647-114">Dans C, l’objet de récepteur advise est composée des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0c647-114">In C, the advise sink object is composed of the following elements:</span></span>
  
- <span data-ttu-id="0c647-115">Pointeur vers un vtable qui contient des pointeurs vers des implémentations de chacune des méthodes dans **IUnknown** et **IMAPIAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="0c647-115">A pointer to a vtable that contains pointers to implementations of each of the methods in **IUnknown** and **IMAPIAdviseSink**.</span></span>
    
- <span data-ttu-id="0c647-116">Membres de données.</span><span class="sxs-lookup"><span data-stu-id="0c647-116">Data members.</span></span>
    
<span data-ttu-id="0c647-117">L’exemple de code suivant montre comment définir l’objet récepteur advise dans C et construire ses vtable.</span><span class="sxs-lookup"><span data-stu-id="0c647-117">The following code example shows how to define an advise sink object in C and construct its vtable.</span></span> 
  
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

<span data-ttu-id="0c647-118">Une fois que vous déclarez un objet C, vous devez l’initialiser en définissant le pointeur vtable à l’adresse de la vtable construite, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="0c647-118">After you declare an object in C, you must initialize it by setting the vtable pointer to the address of the constructed vtable, as shown in the following code:</span></span>
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a><span data-ttu-id="0c647-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c647-119">See also</span></span>

- [<span data-ttu-id="0c647-120">Vue d’ensemble de la propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="0c647-120">MAPI Property Overview</span></span>](mapi-property-overview.md)
- [<span data-ttu-id="0c647-121">Implémentation d’objets MAPI</span><span class="sxs-lookup"><span data-stu-id="0c647-121">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

