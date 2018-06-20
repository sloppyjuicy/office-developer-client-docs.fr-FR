---
title: Section de formulaire Configuration de fichier [plateformes]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ddc6db2303d9d5f114fdb27b6e15e699a04e73f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783345"
---
# <a name="form-configuration-file-platforms-section"></a>Section de formulaire Configuration de fichier [plateformes]

**S’applique à**: Outlook 
  
La section **[plateformes]** répertorie l’ensemble complet des plateformes prises en charge par ce formulaire. Chaque entrée de plateforme comprend le préfixe **plate-forme.** _chaîne_dans laquelle la _chaîne_ est un code de chaîne arbitraire pour la plateforme. Chaque chaîne correspond à l’entrée de **l’UC** de des sections **[plateformes]** . Chaque entrée dans la section **[plateformes]** définit une _chaîne de plateforme_ qui fait référence suivante **[plateforme.** _chaîne de plateforme_ section **]** comme indiqué ici. 
  
La section **[plateformes]** répertorie l’ensemble complet des plateformes prises en charge par ce formulaire. Chaque entrée de plateforme comprend le préfixe **plate-forme.** _chaîne_dans laquelle la _chaîne_ est un code de chaîne arbitraire pour la plateforme. Chaque chaîne correspond à l’entrée de **l’UC** de des sections **[plateformes]** . Chaque entrée dans la section **[plateformes]** définit une _chaîne de plateforme_ qui fait référence suivante **[plateforme.** _chaîne de plateforme_ section **]** comme indiqué ici. 
  
**[Plateformes]**
  
**Plateforme**. _chaîne_ =  _chaîne de plateforme_
  
Voici un exemple d’une section **[plateformes]** . 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

Chaque **[plateforme.** _chaîne de plateforme_ section **]** contient deux entrées obligatoires, **l’UC** et **OSVersion**. L’entrée de **l’UC** Spécifie le processeur et l’entrée **OSVersion** Spécifie le système d’exploitation. Les valeurs de **processeur** valides sont décrits dans le tableau suivant. 
  
|**Entrée de l’UC**|**Processeur**|
|:-----|:-----|
|Ix86  <br/> |Intel x 86 80 et processeurs Pentium, ainsi qu’équivalentes processeurs AMD, Cyrix, NextGen et autres fabricants.  <br/> |
|MIPS  <br/> |Processeurs MIPS R4000.  <br/> |
|AXP  <br/> |Processeur d’équipement Corporation Alpha AXP numériques.  <br/> |
|PPC  <br/> |Processeurs Motorola Power PC.  <br/> |
|M68  <br/> |Processeurs Mororola 68 x 00.  <br/> |
   
Les valeurs valides **OSVersion** sont décrits dans le tableau suivant. 
  
|**Entrée OSVersion**|**Système d'exploitation**|
|:-----|:-----|
|Win3.1  <br/> |Windows 3.1 et Windows pour les groupes de travail 3.11.  <br/> |
|WinNT3.5  <br/> |Windows NT 3.5 ou inférieure.  <br/> |
|Windows 95  <br/> |Windows 95.  <br/> |
|WinNT4.0  <br/> |Windows NT 4.0.  <br/> |
|Mac7  <br/> |Système Macintosh 7.  <br/> |
   
En outre, le **[plateforme.** _chaîne de plateforme_ section **]** doit contenir un **fichier** ou un **liaisonavec** entrée. L’entrée de **fichier** répertorie le formulaire serveur application fichier exécutable qui la bibliothèque de formulaires gère et charge dans un nouveau sous-répertoire dans le cache disque lorsque le formulaire est lancé. Si une entrée **liaisonavec** est utilisée au lieu de cela, elle contient le nom d’une chaîne autre plate-forme d'où provient les informations du **fichier** . Cela est utile si une version d’un formulaire prend en charge plusieurs plates-formes. 
  
L’entrée de **Registre** est utilisée chaque fois que l’entrée de **fichier** est utilisée, il identifie la clé de Registre pour la bibliothèque de formulaires où se trouve le fichier exécutable de l’application de serveur du formulaire. Chaînes précédés d’une barre oblique inverse (\) sont placés à la racine du Registre. Chaînes ne pas précédés d’une barre oblique inverse sont placés dans le _GUID_de HKEY_CLASSES_ROOT\CLSID\ \ clé de Registre, où _GUID_ est le **GUID** du formulaire. Les caractères « %d » peuvent être utilisés pour indiquer le chemin d’accès du répertoire à partir de laquelle le fichier de configuration de formulaire a été lu. Cela est utile pour spécifier d’autres fichiers avec les chemins d’accès par rapport au fichier de configuration de formulaire. Entrées de **Registre** ou de **Plusieurs fichiers** peuvent être spécifiées à l’aide du fichier ou dans le Registre comme préfixe suivi par n’importe quel autre texte. Le format de la **[plateforme.** _chaîne de plateforme_ section **]** est : 
  
- **[Platform.** _chaîne de plateforme_ **]**
    
- **Processeur** =  _chaîne_
    
- **OSVersion** =  _chaîne_
    
- **Fichier** =  _chemin d’accès_
    
- **Liaisonavec** =  _chaîne_
    
- **Registre** =  _chaîne_
  
Voici deux exemples **[plateforme.** _chaîne de plateforme_ sections **]** , à l’aide de l’entrée de **fichier** et un à l’aide de l’entrée **liaisonavec** . 
  
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

Le **[plateforme.** _chaîne de plateforme_ section **]** est ignorée lorsque vous ajoutez un formulaire à la bibliothèque de formulaires local lorsqu’il est supposé que le programme d’installation a placé les fichiers constituant le Gestionnaire de classe de message dans le stockage local disponible en tant que nommé dans la section du gestionnaire dans le Registre OLE et effectué l’inscription OLE dans le Registre du système. 
  

