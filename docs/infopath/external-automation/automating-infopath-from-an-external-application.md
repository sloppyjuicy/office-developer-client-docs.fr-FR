---
title: Automatisation d’InfoPath à partir d’une application externe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath fournit l'automatisation des applications à partir du code écrit à l'aide de COM et du script à l'aide de méthodes de l'objet application et de la collection XDocuments.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412666"
---
# <a name="automating-infopath-from-an-external-application"></a>Automatisation d’InfoPath à partir d’une application externe

Microsoft InfoPath fournit l'automatisation des applications à partir du code écrit à l'aide de COM et du script à l'aide de méthodes de l'objet **application** et de la collection **XDocuments** . 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Vue d'ensemble des objets application et XDocument

L'objet **application** contient les méthodes suivantes utilisées pour Automation: 
  
|**Méthode**|**Description**|
|:-----|:-----|
|**CacheSolution** <br/> |Examine le dans le cache et, si nécessaire, le met à jour à partir de l'emplacement publié du modèle de formulaire.  <br/> |
|**Quit** <br/> |Quitte l'application Microsoft Office InfoPath.  <br/> |
|**RegisterSolution** <br/> |Installe le modèle de formulaire Microsoft Office InfoPath spécifié.  <br/> |
|**UnregisterSolution** <br/> |Désinstalle le modèle de formulaire Microsoft Office InfoPath spécifié.  <br/> |
   
La collection **XDocuments** contient les méthodes suivantes, qui peuvent être utilisées pour l'automatisation externe: 
  
|**Méthode**|**Description**|
|:-----|:-----|
|Méthode **Close**  <br/> |Ferme le formulaire Microsoft Office InfoPath spécifié.  <br/> |
|**New** , méthode  <br/> |Crée un formulaire Microsoft Office InfoPath.  <br/> |
|**NewFromSolution** , méthode  <br/> |Crée un formulaire Microsoft Office InfoPath basé sur le modèle de formulaire spécifié.  <br/> |
|**NewFromSolutionWithData** , méthode  <br/> |Crée un nouveau formulaire Microsoft Office InfoPath en utilisant le modèle de formulaire et les données XML spécifiés.  <br/> |
|**Open** , méthode  <br/> |Ouvre le formulaire Microsoft Office InfoPath spécifié.  <br/> |
   
Pour utiliser l'objet **application** à partir d'une application externe, utilisez la fonction **CreateObject** avec le ProgID de l'application InfoPath («InfoPath. application») pour créer une variable objet qui représente l'application InfoPath. Vous pouvez ensuite utiliser la propriété **XDocuments** pour accéder à la collection **XDocuments** et utiliser ses méthodes pour ouvrir ou créer un formulaire InfoPath. L'exemple suivant illustre la création d'une référence à l'objet **application** à l'aide du langage de programmation Microsoft visual Basic 6,0 ou Visual Basic pour applications (VBA): 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Étant donné que la fonction **CreateObject** crée une variable d'objet à l'aide de la liaison tardive, la saisie semi-automatique des instructions n'est pas disponible dans Visual Basic Editor. RePortez-vous aux liens dans les tableaux précédents pour obtenir des informations sur la syntaxe d'appel correcte. 
  

