---
title: Section [plateformes] du fichier de configuration de formulaire
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419127"
---
# <a name="form-configuration-file-platforms-section"></a>Section [plateformes] du fichier de configuration de formulaire

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Platforms]** répertorie l'ensemble complet des plateformes prises en charge par ce formulaire. Chaque entrée de plateforme se compose de la plateforme de préfixe **.** _String_, où _String_ est un code de chaîne arbitraire pour la plateforme. Chaque chaîne correspond à l'entrée **processeur** d'une section **[Platforms]** individuelle. Chaque entrée dans une section **[Platforms]** définit une _chaîne de plateforme_ qui fait référence à une nouvelle **[plateforme.** _chaîne de plateforme_ **]** , comme illustré ci-dessous. 
  
La section **[Platforms]** répertorie l'ensemble complet des plateformes prises en charge par ce formulaire. Chaque entrée de plateforme se compose de la plateforme de préfixe **.** _String_, où _String_ est un code de chaîne arbitraire pour la plateforme. Chaque chaîne correspond à l'entrée **processeur** d'une section **[Platforms]** individuelle. Chaque entrée dans une section **[Platforms]** définit une _chaîne de plateforme_ qui fait référence à une nouvelle **[plateforme.** _chaîne de plateforme_ **]** , comme illustré ci-dessous. 
  
**Formes**
  
**Plateforme**. __ =  chaîne de_plateforme_ de chaîne
  
Voici un exemple de section **[Platforms]** . 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

Chaque **[plateforme.** _chaîne de plateforme_ **]** contient les deux entrées requises, **CPU** et **OSVersion**. L'entrée **CPU** spécifie le processeur et l'entrée **OSVersion** indique le système d'exploitation. Les valeurs d' **UC** valides sont décrites dans le tableau suivant. 
  
|**Entrée de l'UC**|**Processeur**|
|:-----|:-----|
|Ix86  <br/> |Processeurs Intel 80x86 et Pentium, ainsi que les processeurs équivalents de AMD, Cyrix, NextGen et d'autres fabricants.  <br/> |
|MAUX  <br/> |Processeurs MIPS R4000 Series.  <br/> |
|PLAT  <br/> |Processeur Digital Equipment Corporation Alpha AXP.  <br/> |
|CLIC  <br/> |Processeurs Motorola Power PC Series.  <br/> |
|M68  <br/> |Processeurs mororola série 68x00.  <br/> |
   
Les valeurs valides pour **OSVersion** sont décrites dans le tableau suivant. 
  
|**Entrée OSVersion**|**Système d'exploitation**|
|:-----|:-----|
|Win 3.1  <br/> |Windows 3,1 et Windows pour Workgroups 3,11.  <br/> |
|WinNT 3.5  <br/> |Windows NT 3,5 ou inférieur.  <br/> |
|95  <br/> |Windows 95.  <br/> |
|WinNT 4.0  <br/> |Windows NT 4,0.  <br/> |
|Mac7  <br/> |Macintosh système 7.  <br/> |
   
En outre, **[Platform.** _chaîne de plateforme_ **]** doit contenir un **fichier** ou une entrée **LinkTo** . L'entrée de **fichier** répertorie le fichier exécutable de l'application serveur de formulaires que la bibliothèque de formulaires gère et charge dans un nouveau sous-répertoire du cache disque lors du lancement du formulaire. Si une entrée **LinkTo** est utilisée à la place, elle contient le nom d'une autre chaîne de plateforme à partir de laquelle les informations de **fichier** sont extraites. Cette fonctionnalité est utile si une version d'un formulaire prend en charge plusieurs plateformes. 
  
L'entrée de **Registre** est utilisée chaque fois que l'entrée de **fichier** est utilisée, elle identifie la clé de Registre pour la bibliothèque de formulaires dans laquelle le fichier exécutable de l'application form Server est stocké. Les chaînes précédées d'une barre oblique inverse (\) sont placées à la racine du Registre. Les chaînes qui ne sont pas précédées d'une barre oblique inverse sont placées dans la clé de Registre _GUID_HKEY_CLASSES_ROOT\CLSID\, où _GUID_ est le **GUID** du formulaire. Les caractères «% d» peuvent être utilisés pour indiquer le chemin d'accès du répertoire à partir duquel le fichier de configuration du formulaire a été lu. Cela est utile pour spécifier d'autres fichiers avec des chemins d'accès relatifs au fichier de configuration du formulaire. **Plusieurs** entrées de fichier ou de **registre** peuvent être spécifiées à l'aide du fichier ou du registre en tant que préfixe suivi de tout autre texte. Le format de la **[plateforme.** _chaîne de plateforme_ **]** est la suivante: 
  
- **Plateforme.** _chaîne de plateforme_ **]**
    
- **** =  _Chaîne_ d'UC
    
- **** =  _Chaîne_ OSVersion
    
- **** =  _Chemin d'accès_ du fichier
    
- **** =  _Chaîne_ LinkTo
    
- **** =  _Chaîne_ de Registre
  
Voici deux exemples: **[Platform.** _chaîne de plateforme_ **]** , l'une à l'aide de l'entrée de **fichier** et l'autre à l'aide de l'entrée **LinkTo** . 
  
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

**[Platform.** _chaîne de plateforme_ **]** est ignorée lors de l'ajout d'un formulaire à la bibliothèque de formulaires locale, lorsqu'il est supposé que le programme d'installation a placé les fichiers constituant le gestionnaire de classe de message dans un stockage local disponible tel que nommé dans la section du gestionnaire dans le registre OLE, et a effectué enregistrement OLE dans le Registre du système. 
  

