---
title: Interface ADORecordConstruction (ADO)
TOCTitle: ADORecordConstruction interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2b223e10e6ed8450a881225b76b01761436b12ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607534"
---
# <a name="adorecordconstruction-interface-ado"></a>Interface ADORecordConstruction (ADO)


**S’applique à** : Access 2013, Office 2013

L'interface **ADORecordConstruction** permet de créer un objet **Record** ADO à partir d'un objet **Row** OLE DB dans une application C/C++.

Cette interface prend en charge les propriétés ci-après :

## <a name="properties"></a>Propriétés

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="parentrow-property-ado.md">ParentRow</a></p></td>
<td><p>En écriture seule.<br />

Définit le conteneur d'un objet <strong>Row</strong> OLE DB sur cet objet <strong>Record</strong> ADO.</p></td>
</tr>
<tr class="even">
<td><p><a href="row-property-ado.md">Ligne</a></p></td>
<td><p>Lecture/écriture.<br />
 Extrait/définit un objet <strong>Row</strong> OLE DB de/sur cet objet <strong>Record</strong> ADO.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Méthodes

Aucun.

## <a name="events"></a>Événements

Aucun.

## <a name="remarks"></a>Remarques

Étant donné un objet row OLE **DB** (pRow), la construction d’un objet **Record** ADO (), la construction d’un objet **Record** ADO (adoR), revient aux trois opérations de base suivantes :

1.  Créez un objet ADO **Record**:
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  Interrogez l'interface **IADORecordConstruction** sur l'objet **Record**:
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  Appelez la méthode de propriété **IADORecordConstruction::p ut \_ Row** pour définir l’objet Row OLE **DB** sur l’objet **Record** ADO :
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
L'objet **adoR** qui en résulte représente maintenant l'objet **Record** ADO créé à partir de l'objet **Row** OLE DB.

Un objet **Record** ADO peut également être créé à partir du conteneur d'un objet **Row** OLE DB.

## <a name="requirements"></a>Configuration requise

**Version :** ADO 2.0 et supérieure

**Bibliothèque :** msado15.dll

**UUID :** 00000567-0000-0010-8000-00AA006D2EA4

