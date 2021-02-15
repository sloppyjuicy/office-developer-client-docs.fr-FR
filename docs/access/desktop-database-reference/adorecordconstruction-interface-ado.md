---
title: Interface ADORecordConstruction (ADO)
TOCTitle: ADORecordConstruction interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a53eb107bab0d31606dc161b9f9c910894c5bc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281625"
---
# <a name="adorecordconstruction-interface-ado"></a><span data-ttu-id="639b8-102">Interface ADORecordConstruction (ADO)</span><span class="sxs-lookup"><span data-stu-id="639b8-102">ADORecordConstruction interface (ADO)</span></span>


<span data-ttu-id="639b8-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="639b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="639b8-104">L'interface **ADORecordConstruction** permet de créer un objet **Record** ADO à partir d'un objet **Row** OLE DB dans une application C/C++.</span><span class="sxs-lookup"><span data-stu-id="639b8-104">The **ADORecordConstruction** interface is used to construct an ADO **Record** object from an OLE DB **Row** object in a C/C++ application.</span></span>

<span data-ttu-id="639b8-105">Cette interface prend en charge les propriétés ci-après :</span><span class="sxs-lookup"><span data-stu-id="639b8-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="639b8-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="639b8-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="639b8-107"><a href="parentrow-property-ado.md">ParentRow</a></span><span class="sxs-lookup"><span data-stu-id="639b8-107"><a href="parentrow-property-ado.md">ParentRow</a></span></span></p></td>
<td><p><span data-ttu-id="639b8-108">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="639b8-108">Write-only.</span></span><br />
<span data-ttu-id="639b8-109">
Définit le conteneur d'un objet <strong>Row</strong> OLE DB sur cet objet <strong>Record</strong> ADO.</span><span class="sxs-lookup"><span data-stu-id="639b8-109">Sets the container of an OLE DB <strong>Row</strong> object on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="639b8-110"><a href="row-property-ado.md">Ligne</a></span><span class="sxs-lookup"><span data-stu-id="639b8-110"><a href="row-property-ado.md">Row</a></span></span></p></td>
<td><p><span data-ttu-id="639b8-111">Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="639b8-111">Read/Write.</span></span><br />
<span data-ttu-id="639b8-112"> Extrait/définit un objet <strong>Row</strong> OLE DB de/sur cet objet <strong>Record</strong> ADO.</span><span class="sxs-lookup"><span data-stu-id="639b8-112">Gets/sets an OLE DB <strong>Row</strong> object from/on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="639b8-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="639b8-113">Methods</span></span>

<span data-ttu-id="639b8-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="639b8-114">None.</span></span>

## <a name="events"></a><span data-ttu-id="639b8-115">Événements</span><span class="sxs-lookup"><span data-stu-id="639b8-115">Events</span></span>

<span data-ttu-id="639b8-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="639b8-116">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="639b8-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="639b8-117">Remarks</span></span>

<span data-ttu-id="639b8-118">Étant donné un objet row OLE **DB** (pRow), la construction d’un objet **Record** ADO (), la construction d’un objet **Record** ADO (adoR), revient aux trois opérations de base suivantes :</span><span class="sxs-lookup"><span data-stu-id="639b8-118">Given an OLE DB **Row** object (pRow), the construction of an ADO **Record** object (), the construction of an ADO **Record** object (adoR), amounts to the following three basic operations:</span></span>

1.  <span data-ttu-id="639b8-119">Créez un objet ADO **Record**:</span><span class="sxs-lookup"><span data-stu-id="639b8-119">Create an ADO **Record** object:</span></span>
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  <span data-ttu-id="639b8-120">Interrogez l'interface **IADORecordConstruction** sur l'objet **Record**:</span><span class="sxs-lookup"><span data-stu-id="639b8-120">Query the **IADORecordConstruction** interface on the **Record** object:</span></span>
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  <span data-ttu-id="639b8-121">Appelez la méthode de propriété **IADORecordConstruction::p ut \_ Row** pour définir l’objet row OLE **DB** sur l’objet **Record** ADO :</span><span class="sxs-lookup"><span data-stu-id="639b8-121">Call the **IADORecordConstruction::put\_Row** property method to set the OLE DB **Row** object on the ADO **Record** object:</span></span>
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
<span data-ttu-id="639b8-122">L'objet **adoR** qui en résulte représente maintenant l'objet **Record** ADO créé à partir de l'objet **Row** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="639b8-122">The resultant **adoR** object now represents the ADO **Record** object constructed from the OLE DB **Row** object.</span></span>

<span data-ttu-id="639b8-123">Un objet **Record** ADO peut également être créé à partir du conteneur d'un objet **Row** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="639b8-123">An ADO **Record** object can also be constructed from the container of an OLE DB **Row** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="639b8-124">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="639b8-124">Requirements</span></span>

<span data-ttu-id="639b8-125">**Version :** ADO 2.0 et supérieure</span><span class="sxs-lookup"><span data-stu-id="639b8-125">**Version:** ADO 2.0 and later</span></span>

<span data-ttu-id="639b8-126">**Bibliothèque :** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="639b8-126">**Library:** msado15.dll</span></span>

<span data-ttu-id="639b8-127">**UUID :** 00000567-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="639b8-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span></span>

