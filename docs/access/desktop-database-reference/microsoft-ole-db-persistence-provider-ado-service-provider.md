---
title: Fournisseur de persistance Microsoft OLE DB (fournisseur de service ADO)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9a9a7141adab06024e2f7f44df329ced59c3e35a
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629873"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a>Fournisseur de persistance Microsoft OLE DB (fournisseur de services ADO)


**S’applique à** : Access 2013, Office 2013 

The Microsoft OLE DB Persistence Provider enables you to save a [Recordset](recordset-object-ado.md) object into a file, and later restore that **Recordset** object from the file. Schema information, data, and pending changes are preserved.

Vous pouvez enregistrer le **Recordset** au format ADTG (Advanced Data Table Gram) ou au format XML ouvert (Extensible Markup Language).

## <a name="provider-keyword"></a>Mot clé du fournisseur

Pour appeler ce fournisseur, spécifiez le mot clé et la valeur suivants dans la chaîne de connexion.

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a>Erreurs

Les erreurs suivantes émises par ce fournisseur peuvent être détectées dans votre application.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>E_BADSTREAM</p></td>
<td><p>Le fichier ouvert n'a pas un format valide (c'est-à-dire que son format n'est ni ADTG, ni XML ).</p></td>
</tr>
<tr class="even">
<td><p>E_CANTPERSISTROWSET</p></td>
<td><p>L'objet <strong>Recordset</strong> enregistré présente des caractéristiques qui l'empêchent d'être stocké.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Le fournisseur de persistance Microsoft OLE DB n’expose pas de propriétés dynamiques.

Actuellement, seuls les objets **Recordset** hiérarchiques paramétrés ne peuvent pas être enregistrés.

Pour plus d’informations sur le stockage persistant des objets **Recordset**, consultez la rubrique [Informations complémentaires sur la persistance des objets Recordset](more-about-recordset-persistence.md).

Lorsqu'un flux est utilisé pour ouvrir un **Recordset**, seul le paramètre *Source* de la méthode **Open** doit être spécifié.

