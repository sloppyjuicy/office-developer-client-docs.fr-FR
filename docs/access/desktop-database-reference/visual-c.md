---
title: Visual C++ (référence de base de données du bureau Access)
TOCTitle: Visual C++
ms:assetid: 31d27968-e7bd-02fa-efad-26039bea30b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249091(v=office.15)
ms:contentKeyID: 48544062
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e6f0e020373db9bf0fe7acc1b1c7bfeab210329
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861420"
---
# <a name="visual-c"></a><span data-ttu-id="0fb4f-102">Visual C++</span><span class="sxs-lookup"><span data-stu-id="0fb4f-102">Visual C++</span></span>


<span data-ttu-id="0fb4f-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0fb4f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0fb4f-104">Ceci est une description schématique de la manière de créer une instance d'événements ADO dans Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-104">This is a schematic description of how to instantiate ADO events in Microsoft Visual C++.</span></span> <span data-ttu-id="0fb4f-105">Voir [l’exemple de modèle d’événements ADO (VC ++)](ado-events-model-example-vc.md) pour une description complète.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-105">See [ADO Events Model example (VC++)](ado-events-model-example-vc.md) for a complete description.</span></span>

<span data-ttu-id="0fb4f-106">Créez des classes dérivées des interfaces **ConnectionEventsVt** et **RecordsetEventsVt** du fichier adoint.h.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-106">Create classes derived from the **ConnectionEventsVt** and **RecordsetEventsVt** interfaces found in the file adoint.h.</span></span>

```cpp 
 
// BeginEventExampleVC01 
class CConnEvent : public ConnectionEventsVt 
{ 
 public: 
 STDMETHODIMP InfoMessage( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection); 
... 
} 
 
class CRstEvent : public RecordsetEventsVt 
{ 
 public: 
 STDMETHODIMP WillChangeField( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset); 
... 
} 
// EndEventExampleVC01 
```

<span data-ttu-id="0fb4f-107">Implémentez chaque méthode de gestionnaire d'événements dans les deux classes.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-107">Implement each of the event-handler methods in both classes.</span></span> <span data-ttu-id="0fb4f-108">Il suffit que chaque méthode retourne simplement une valeur HRESULT de S\_OK.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-108">It is sufficient that each method merely return an HRESULT of S\_OK.</span></span> <span data-ttu-id="0fb4f-109">Cependant, lorsque la disponibilité de vos gestionnaires d'événements est connue, ils sont sans cesse invoqués par défaut.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-109">However, when you make it known that your event handlers are available, they will be called continuously by default.</span></span> <span data-ttu-id="0fb4f-110">Vous pouvez toutefois décider d'annuler toute notification ultérieure la première fois en définissant **adStatus** sur **adStatusUnwantedEvent**.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-110">Instead, you might want to request no further notification after the first time by setting **adStatus** to **adStatusUnwantedEvent**.</span></span>

```cpp 
 
// BeginEventExampleVC02 
STDMETHODIMP CConnEvent::ConnectComplete( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
// EndEventExampleVC02 
```

<span data-ttu-id="0fb4f-p103">Les classes d'événements héritent de **IUnknown**; vous devez donc aussi implémenter les méthodes **QueryInterface**, **AddRef** et **Release**, ainsi que des constructeurs et destructeurs de classes. Choisissez les outils Visual C++ que vous maîtrisez le mieux pour simplifier cette partie de la tâche.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-p103">The event classes inherit from **IUnknown**, so you must also implement the **QueryInterface**, **AddRef**, and **Release** methods. Also implement class constructors and destructors. Choose the Visual C++ tools with which you are most comfortable to simplify this part of the task.</span></span>

<span data-ttu-id="0fb4f-p104">Diffusez la disponibilité de vos gestionnaires d'événements en publiant **QueryInterface** sur les objets [Recordset](recordset-object-ado.md) et [Connection](connection-object-ado.md) des interfaces **IConnectionPointContainer** et **IConnectionPoint**. Ensuite, publiez **IConnectionPoint::Advise** pour chaque classe.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-p104">Make it known that your event handlers are available by issuing **QueryInterface** on the [Recordset](recordset-object-ado.md) and [Connection](connection-object-ado.md) objects for the **IConnectionPointContainer** and **IConnectionPoint** interfaces. Then issue **IConnectionPoint::Advise** for each class.</span></span>

<span data-ttu-id="0fb4f-116">Par exemple, supposons que vous utilisez une fonction booléenne qui renvoie **True** si elle informe bien un objet **Recordset** de la disponibilité de vos gestionnaires d'événements.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-116">For example, assume you are using a Boolean function that returns **True** if it successfully informs a **Recordset** object that you have event handlers available.</span></span>

```cpp 
 
// BeginEventExampleVC03 
HRESULT hr; 
DWORD dwEvtClass; 
IConnectionPointContainer *pCPC = NULL; 
IConnectionPoint *pCP = NULL; 
CRstEvent *pRStEvent = NULL; 
... 
_RecordsetPtr pRs; 
pRs.CreateInstance(__uuidof(Recordset)); 
pRStEvent = new CRstEvent; 
if (pRStEvent == NULL) return FALSE; 
... 
hr = pRs->QueryInterface(IID_IConnectionPointContainer, (LPVOID *)&pCPC); 
if (FAILED(hr)) return FALSE; 
hr = pCPC->FindConnectionPoint(RecordsetEvents, &pCP); 
pCPC->Release(); // Always Release now, even before checking. 
if (FAILED(hr)) return FALSE; 
hr = pCP->Advise(pRstEvent, &dwEvtClass); //Turn on event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
return TRUE; 
... 
// EndEventExampleVC03 
```

<span data-ttu-id="0fb4f-117">À ce stade, les événements de la famille **RecordsetEvent** sont activés et vos méthodes seront invoquées dès qu'un événement **Recordset** survient.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-117">At this point, events for the **RecordsetEvent** family are enabled and your methods will be called as **Recordset** events occur.</span></span>

<span data-ttu-id="0fb4f-118">Si vous souhaitez ensuite annuler la disponibilité de vos gestionnaires d'événements, retournez au point de connexion et publiez la méthode **IConnectionPoint::Unadvise**.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-118">Later, when you want to make your event handlers unavailable, get the connection point again and issue the **IConnectionPoint::Unadvise** method.</span></span>

```cpp 
 
// BeginEventExampleVC04 
... 
hr = pCP->Unadvise(dwEvtClass); //Turn off event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
// EndEventExampleVC04 
```

<span data-ttu-id="0fb4f-119">Vous devez publier les interfaces et détruire les objets de classe selon les circonstances.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-119">You must release interfaces and destroy class objects as appropriate.</span></span>

<span data-ttu-id="0fb4f-120">Le code suivant illustre un exemple complet d'une classe de réception d'événement **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-120">The following code shows a complete example of a **Recordset** Event sink class.</span></span>

```vb 
 
// BeginEventExampleVC05 
#include <adoint.h> 
 
class CADORecordsetEvents : public RecordsetEventsVt 
{ 
public : 
 
 ULONG m_ulRefCount; 
 CADORecordsetEvents():m_ulRefCount(1){} 
 
 STDMETHOD(QueryInterface)(REFIID iid, LPVOID * ppvObject) 
 { 
 if (IsEqualIID(__uuidof(IUnknown), iid) || 
 IsEqualIID(__uuidof(RecordsetEventsVt), iid)) 
 { 
 *ppvObject = this; 
 return S_OK; 
 } 
 else 
 return E_NOINTERFACE; 
 } 
 
 STDMETHOD_(ULONG, AddRef)() 
 { 
 return m_ulRefCount++; 
 } 
 
 STDMETHOD_(ULONG, Release)() 
 { 
 if (--m_ulRefCount == 0) 
 { 
 delete this; 
 return 0; 
 } 
 else 
 return m_ulRefCount; 
 } 
 
 
 STDMETHOD(WillChangeField)( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FieldChangeComplete)( 
 LONG cFields, 
 VARIANT Fields, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(WillChangeRecord)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(RecordChangeComplete)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillChangeRecordset)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(RecordsetChangeComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillMove)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(MoveComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(EndOfRecordset)( 
 VARIANT_BOOL *fMoreData, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FetchProgress)( 
 long Progress, 
 long MaxProgress, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(FetchComplete)( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
}; 
// EndEventExampleVC05 
```

