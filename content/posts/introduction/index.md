---
title: "Teste Commit"
date: 2020-06-08T08:06:25+06:00
description: Introduction to Sample Post
menu:
  sidebar:
    name: PRIMEIRO
    identifier: introduction
    weight: 10
tags: ["Basic", "Multi-lingual"]
categories: ["Basic"]
---


package main

import (
	"fmt"
	"io/ioutil"
	"net/http"
)

func main() {
	// URL da página externa que você deseja carregar
	url := "https://medium.com/itnext/building-a-ci-cd-pipeline-for-a-serverless-express-application-with-aws-cdk-1d3c842ea1ff"

	// Faça uma solicitação HTTP GET para a URL
	resp, err := http.Get(url)
	if err != nil {
		fmt.Println("Erro ao fazer a solicitação HTTP:", err)
		return
	}
	defer resp.Body.Close()

	// Verifique o código de status da resposta
	if resp.StatusCode != http.StatusOK {
		fmt.Println("Erro: Status Code", resp.StatusCode)
		return
	}

	// Leia o conteúdo da resposta
	body, err := ioutil.ReadAll(resp.Body)
	if err != nil {
		fmt.Println("Erro ao ler o corpo da resposta:", err)
		return
	}

	// Exiba o conteúdo da página externa
	fmt.Println(string(body))
}


G# Título do Documento

Este é um exemplo de um arquivo Markdown. Você pode usar o Markdown para criar documentos de texto formatados de maneira simples e fácil.

## Lista de Itens

- Item 1
- Item 2
- Item 3

## Links

Você pode criar [links](https://medium.com/itnext/building-a-ci-cd-pipeline-for-a-serverless-express-application-with-aws-cdk-1d3c842ea1ff) para outros sites.

## Imagens

Você pode incorporar imagens também:

![Imagem de Exemplo](imagem.jpg)

## Formatação de Texto

Você pode *enfatizar* palavras ou **realçar** textos facilmente.

## Blocos de Código

Você pode incluir blocos de código em seu documento:

```python
def exemplo():
    print("Isso é um exemplo de código.")

