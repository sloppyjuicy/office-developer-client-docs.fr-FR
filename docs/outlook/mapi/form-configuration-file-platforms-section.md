---
title: Section Fichier de configuration de formulaire [Plateformes]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d1c69a38c0da1bd9a048e63c7ada005d88293d7a
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773753"
---
# <a name="form-configuration-file-platforms-section"></a>Section Fichier de configuration de formulaire [Plateformes]

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Plateformes]** répertorie l’ensemble complet des plateformes pris en charge par ce formulaire. Chaque entrée de plateforme se compose du **préfixe Platform.** _chaîne_, où  _chaîne_ est un code de chaîne arbitraire pour la plateforme. Chaque chaîne correspond à l’entrée **processeur** d’une section **[Plateformes]** individuelle. Chaque entrée d’une section **[Plateformes]** définit une  chaîne de plateforme qui fait référence à une **autre [plateforme.** _section chaîne de_ **plateforme ]** comme illustré ici. 
  
La section **[Plateformes]** répertorie l’ensemble complet des plateformes pris en charge par ce formulaire. Chaque entrée de plateforme se compose du **préfixe Platform.** _chaîne_, où  _chaîne_ est un code de chaîne arbitraire pour la plateforme. Chaque chaîne correspond à l’entrée **processeur** d’une section **[Plateformes]** individuelle. Chaque entrée d’une section **[Plateformes]** définit une  chaîne de plateforme qui fait référence à une **autre [plateforme.** _section chaîne de_ **plateforme ]** comme illustré ici. 
  
**[Plateformes]**
  
**Plateforme**. _string_ =   _chaîne de plateforme_
  
Voici un exemple de section **[Plateformes** ]. 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

Chaque **[plateforme.** _section chaîne de_ **plateforme ]** contient les deux entrées requises, **processeur** et **OSVersion**. **L’entrée du** processeur spécifie le processeur et l’entrée **OSVersion** spécifie le système d’exploitation. Les **valeurs de** processeur valides sont décrites dans le tableau suivant. 
  
|**Entrée processeur**|**Processeur**|
|:-----|:-----|
|Ix86  <br/> |Processeurs de série Intel 80x86 et Pentium, ainsi que des processeurs équivalents d’AMD, Cyrix, NextGen et d’autres fabricants. |
|MIPS  <br/> |Processeurs de série MIPS R4000. |
|AXP  <br/> |Processeur Alpha AXP Digital Equipment Corporation. |
|CPP  <br/> |Processeurs de série Power PC. |
|M68  <br/> |Processeurs série 68 x 00. |
   
Les valeurs **OSVersion** valides sont décrites dans le tableau suivant. 
  
|**Entrée OSVersion**|**Système d'exploitation**|
|:-----|:-----|
|Win3.1  <br/> |Windows 3.1 et Windows workgroups 3.11. |
|WinNT3.5  <br/> |Windows NT 3.5 ou inférieure. |
|Win95  <br/> |Windows 95. |
|WinNT4.0  <br/> |Windows NT 4.0. |
|Mac7  <br/> |Système Macintosh 7. |
   
En outre, la **[plateforme.** _la section chaîne_ **de plateforme ]** doit contenir une **entrée Fichier** ou **LinkTo** . **L’entrée** Fichier répertorie le fichier exécutable de l’application serveur de formulaires que la bibliothèque de formulaires tient à jour et charge dans un nouveau sous-dossier dans le cache disque lors du lancement du formulaire. Si une **entrée LinkTo** est utilisée à la place, elle contient le nom d’une chaîne de plateforme différente à partir de laquelle les informations **de** fichier sont prises. Cela est utile si une version d’un formulaire prend en charge plusieurs plateformes. 
  
**L’entrée** de Registre est utilisée chaque  fois que l’entrée de fichier est utilisée, elle identifie la clé de Registre de la bibliothèque de formulaires dans laquelle le fichier exécutable de l’application de serveur de formulaires est stocké. Les chaînes précédées d’une barre oblique inverse ( \ ) sont placées à la racine du Registre. Les chaînes qui ne sont pas précédées d’une barre oblique inverse sont placées dans la clé HKEY_CLASSES_ROOT\CLSID\  _GUID_\, où  _GUID_ est le **GUID** du formulaire. Les caractères « %d » peuvent être utilisés pour indiquer le chemin d’accès du répertoire à partir duquel le fichier de configuration du formulaire a été lu. Cela est utile pour spécifier d’autres fichiers avec des noms de chemin d’accès relatifs au fichier de configuration du formulaire. **Plusieurs entrées** de fichier ou de **Registre** peuvent être spécifiées en utilisant Fichier ou Registre comme préfixe suivi de tout autre texte. Format de **la [plateforme.** _la section chaîne de_ **plateforme ]** est la suivante : 
  
- **[Plateforme.** _chaîne de plateforme_ **]**
    
- **UC** =   _string_
    
- **OSVersion** =   _string_
    
- **Fichier** =   _chemin d’accès_
    
- **LinkTo** =   _string_
    
-  =   Registre _string_
  
Voici deux exemples **[Plateforme.** _sections de chaîne_ **de plateforme ]** : une à l’aide de **l’entrée Fichier** et une autre à l’entrée **LinkTo** . 
  
```cpp
[Platform.NTx86]
CPU = ix86
OSVersion = WinNT3.5
File = \helpdesk.exe
Registry = Local Server = %d\helpdesk.exe
[Platform.Win95]
CPU = ix86
OSVersion = Win95
LinkTo = NTx86

```

[ **Plateforme.**  la section chaîne de plateforme **]** est ignorée lors de l’ajout d’un formulaire à la bibliothèque de formulaires locale, lorsqu’il est supposé que le programme d’installation a placé les fichiers en charge du handler de classe de message dans le stockage local disponible, comme indiqué dans la section du responsable dans le Registre OLE, et a effectué l’inscription OLE dans le Registre du système. 
  

