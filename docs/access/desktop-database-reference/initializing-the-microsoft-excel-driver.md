---
title: Initialisation du pilote Microsoft Excel
TOCTitle: Initializing the Microsoft Excel driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 92155a8329c137631c1c808019c1ecd7e9912836
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632097"
---
# <a name="initializing-the-microsoft-excel-driver"></a>Initialisation du pilote Microsoft Excel

**S’applique** à : Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office entreprise Access 2013 | Excel 2010 | Access 2010

Lorsque vous installez le pilote Excel, le programme d’installation écrit un ensemble de valeurs par défaut dans le Registre Windows dans les sous-clés Engines et ISAM Formats. Vous ne devez pas modifier ces paramètres directement ; utilisez le programme d’installation de votre application pour ajouter, supprimer ou modifier ces paramètres. Les sections suivantes décrivent l’initialisation et les paramètres de format ISAM pour le pilote Microsoft Excel base de données.

## <a name="excel-initialization-settings"></a>Excel d’initialisation

Le **dossier Access Connectivity EngineEngines\\\\ Excel** inclut les paramètres d’initialisation du pilote Aceexcl.dll, utilisé pour l’accès externe Microsoft Excel feuilles de calcul. L'exemple ci-après montre des paramètres par défaut pour les entrées de ce dossier.

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

Le moteur de base de données Microsoft Access utilise les entrées de dossier Excel suivantes.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Entrée</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>win32</p></td>
<td><p>Emplacement de msexcl40.dll. Le Chemin d'accès complet est déterminé au moment de l'installation. Les valeurs sont de type REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>TypeGuessRows</p></td>
<td><p>Nombre de lignes à vérifier pour le type de données. Celui-ci est déterminé en fonction du nombre maximal de types de données trouvés. En cas d'égalité, le type de données est déterminé dans l'ordre suivant : Numérique, Monétaire, Date, Texte, Booléen. Si les données rencontrées ne correspondent pas au type de données déterminé pour la colonne, une valeur  <strong>Null </strong> est renvoyée. Lors de l'importation, si une colonne a mélangé des type de données, la colonne entière sera mise en forme en fonction du paramètre ImportMixedTypes. Le nombre de lignes par défaut à vérifier est de 8. Les valeurs sont de type REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>ImportMixedTypes</p></td>
<td><p>Peut être défini avec la valeur MajorityType ou Text. Avec MajorityType, les colonnes de types de données mélangés sont mises en forme en fonction du type de données prédominant à l'importation. Avec Text, elles seront mises en forme selon le type de données texte à l'importation. La valeur par défaut est Text. Les values sont de type REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>AppendBlankRows</p></td>
<td><p>Nombre de lignes vides devant être ajouté à la fin d'une feuille de calcul version 3.5 ou 4.0, avant l'ajout de nouvelles données. Par exemple, si AppendBlankRows possède la valeur 4, Microsoft Jet ajoutera 4 lignes vides à la fin de la feuille de calcul avant d'ajouter les lignes qui contiennent des données. Les valeurs entières pour ce paramètre peuvent être comprises entre 0 entre 16 ; la valeur par défaut est 01 (une ligne supplémentaire). Les valeurs sont de type REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Valeur binaire qui indique si la première ligne du tableau contient des noms de colonne. La valeur 01 indique que les noms de colonne sont pris de la première ligne, pendant l'importation. La valeur 00 indique l'absence de nom de colonne dans la première ligne ; les noms de colonne sont alors F1, F2, F3 etc. La valeur par défaut est 01. Les valeurs sont de type REG_BINARY.</p></td>
</tr>
</tbody>
</table>


Le **dossier Access Connectivity EngineEngines\\\\ Excel 8.0** contient les entrées suivantes, qui s’appliquent Microsoft Excel 97.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom d'entrée</p></th>
<th><p>Type</p></th>
<th><p>Valeur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Moteur</p></td>
<td><p>REG_SZ</p></td>
<td><p>Excel</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Microsoft Excel 97-2000 (*.xls)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Permet d'exporter les données de la base de données active vers le fichier Microsoft Excel 97. Ce processus entraîne l'écrasement des données si l'exportation a lieu vers un fichier existant.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>


## <a name="using-the-typeguessrows-setting-for-excel-driver"></a>Utilisation du paramètre TypeGuessRows pour Excel pilote
Lorsque vous utilisez Microsoft Excel driver, vous pouvez utiliser la valeur de Registre **TypeGuessRows** pour configurer le nombre de lignes à vérifier pour le type de données. La **valeur TypeGuessRows se** trouve sous la sous-clé de Registre suivante :

# <a name="office-2016"></a>[Office 2016](#tab/office-2016)

Pour une installation MSI de Office

- Pour les Office 32 bits sur des Windows 32 bits ou des Office 64 bits sur des Windows 64 bits :
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

- Pour les Office 32 bits sur des Windows 64 bits :

  **HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**
    
Pour une installation « En un clic de Office

- Pour les Office 32 bits sur des Windows 32 bits ou des Office 64 bits sur des Windows 64 bits :
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

- Pour les Office 32 bits sur des Windows 64 bits :
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

Le nombre par défaut de lignes à vérifier est **8** (huit). Lorsque vous définissez la valeur **TypeGuessRows** sur **0** (zéro), Excel Driver vérifie le type de données sur les 16 384 premières lignes. Si vous souhaitez vérifier plus de 16 384 lignes, définissez **TypeGuessRows** sur une valeur basée sur la plage souhaitée. Pour vérifier toutes les lignes, définissez **TypeGuessRows** sur 1 048 576 (nombre maximal de lignes autorisées dans Excel).
 
Le type de données est déterminé par le nombre maximal de types de données trouvés. En cas d’égalité, le type de données est déterminé dans l’ordre suivant :

- Nombre
- Devise
- Date
- Text
- Boolean

Si des données rencontrées ne correspondent pas au type de données de estimation pour la colonne, ces données sont renvoyées sous forme **de valeur Null** . Lors d’une importation, si une colonne possède des types de données mixtes, la colonne entière est castée vers le type de données qui est définie par le paramètre **ImportMixedTypes** .

# <a name="office-2013"></a>[Office 2013](#tab/office-2013)

Pour les Office 32 bits sur des Windows 32 bits ou des Office 64 bits sur des Windows 64 bits :

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

Pour les Office 32 bits sur des Windows 64 bits :

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

Le nombre par défaut de lignes à vérifier est **8** (huit). Lorsque vous définissez la valeur **TypeGuessRows** sur **0** (zéro), Excel Driver vérifie le type de données sur les 16 384 premières lignes. Si vous souhaitez vérifier plus de 16 384 lignes, définissez **TypeGuessRows** sur une valeur basée sur la plage souhaitée. Pour vérifier toutes les lignes, définissez **TypeGuessRows** sur 1 048 576 (nombre maximal de lignes autorisées dans Excel).
 
Le type de données est déterminé par le nombre maximal de types de données trouvés. En cas d’égalité, le type de données est déterminé dans l’ordre suivant :

- Nombre
- Devise
- Date
- Text
- Booléen

Si des données rencontrées ne correspondent pas au type de données de estimation pour la colonne, ces données sont renvoyées sous forme **de valeur Null** . Lors d’une importation, si une colonne possède des types de données mixtes, la colonne entière est castée vers le type de données qui est définie par le paramètre **ImportMixedTypes** .

# <a name="office-2010"></a>[Office 2010](#tab/office-2010)

Pour les Office 32 bits sur des Windows 32 bits ou des Office 64 bits sur des Windows 64 bits :

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

Pour les Office 32 bits sur des Windows 64 bits :

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

Le nombre par défaut de lignes à vérifier est **8** (huit). Lorsque vous définissez la valeur **TypeGuessRows** sur **0** (zéro), Excel Driver vérifie le type de données sur les 16 384 premières lignes. Si vous souhaitez vérifier plus de 16 384 lignes, définissez **TypeGuessRows** sur une valeur basée sur la plage souhaitée. Pour vérifier toutes les lignes, définissez **TypeGuessRows** sur 1 048 576 (nombre maximal de lignes autorisées dans Excel).
 
Le type de données est déterminé par le nombre maximal de types de données trouvés. En cas d’égalité, le type de données est déterminé dans l’ordre suivant :

- Nombre
- Devise
- Date
- Text
- Booléen

Si des données rencontrées ne correspondent pas au type de données de estimation pour la colonne, ces données sont renvoyées sous forme **de valeur Null** . Lors d’une importation, si une colonne possède des types de données mixtes, la colonne entière est castée vers le type de données qui est définie par le paramètre **ImportMixedTypes** .

---
> [!NOTE]
> [!REMARQUE] Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.

## <a name="see-also"></a>Consultez aussi

- [Utilisation du paramètre TypeGuessRows pour Excel pilote](https://support.office.com/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)

