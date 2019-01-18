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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712007"
---
# <a name="adorecordconstruction-interface-ado"></a>Interface ADORecordConstruction (ADO)


**S’applique à**: Access 2013, Office 2013

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
Définit le conteneur d’un objet OLE DB <strong>Row</strong> sur cet objet ADO <strong>Record</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="row-property-ado.md">Ligne</a></p></td>
<td><p>Lecture/écriture.<br />
Obtient ou définit un objet OLE DB <strong>Row</strong> à partir de/sur cet objet ADO <strong>Record</strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Méthodes

Aucune.

## <a name="events"></a>Événements

Aucun.

## <a name="remarks"></a>Remarques

Étant donné un objet OLE DB **Row** (pRow), la construction d’un objet de ADO **Record** (), la construction d’un objet ADO **Record** (adoR), les chiffres à trois opérations ci-après :

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

3.  Appelez le **IADORecordConstruction::put\_ligne** méthode de la propriété pour définir l’objet OLE DB **Row** dans l’objet ADO **Record** :
    
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

