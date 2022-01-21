<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>
  <meta itemprop="name" content="robomimic_ph" />
  <meta itemprop="description" content="The Proficient Human datasets were collected by 1 proficient operator using the&#10;[RoboTurk](https://roboturk.stanford.edu/) platform (with the exception of&#10;Transport, which had 2 proficient operators working together). Each dataset&#10;consists of 200 successful trajectories.&#10;&#10;Each task has two versions: one with low dimensional observations (`low_dim`),&#10;and one with images (`image`).&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;robomimic_ph&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/robomimic_ph" />
  <meta itemprop="sameAs" content="https://arise-initiative.github.io/robomimic-web/" />
  <meta itemprop="citation" content="@inproceedings{robomimic2021,&#10;  title={What Matters in Learning from Offline Human Demonstrations for Robot Manipulation},&#10;  author={Ajay Mandlekar and Danfei Xu and Josiah Wong and Soroush Nasiriany&#10;          and Chen Wang and Rohun Kulkarni and Li Fei-Fei and Silvio Savarese&#10;          and Yuke Zhu and Roberto Mart&#x27;{i}n-Mart&#x27;{i}n},&#10;  booktitle={arXiv preprint arXiv:2108.03298},&#10;  year={2021}&#10;}" />
</div>

# `robomimic_ph`


Note: This dataset was added recently and is only available in our
`tfds-nightly` package
<span class="material-icons" title="Available only in the tfds-nightly package">nights_stay</span>.

*   **Description**:

The Proficient Human datasets were collected by 1 proficient operator using the
[RoboTurk](https://roboturk.stanford.edu/) platform (with the exception of
Transport, which had 2 proficient operators working together). Each dataset
consists of 200 successful trajectories.

Each task has two versions: one with low dimensional observations (`low_dim`),
and one with images (`image`).

*   **Homepage**:
    [https://arise-initiative.github.io/robomimic-web/](https://arise-initiative.github.io/robomimic-web/)

*   **Source code**:
    [`tfds.robomimic.robomimic_ph.RobomimicPh`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/robomimic/robomimic_ph/robomimic_ph.py)

*   **Versions**:

    *   **`1.0.0`** (default): Initial release.

*   **Download size**: `Unknown size`

*   **Dataset size**: `Unknown size`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Unknown

*   **Splits**:

Split | Examples
:---- | -------:

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `None`

*   **Figure**
    ([tfds.show_examples](https://www.tensorflow.org/datasets/api_docs/python/tfds/visualization/show_examples)):
    Not supported.

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):
    Missing.

*   **Citation**:

```
@inproceedings{robomimic2021,
  title={What Matters in Learning from Offline Human Demonstrations for Robot Manipulation},
  author={Ajay Mandlekar and Danfei Xu and Josiah Wong and Soroush Nasiriany
          and Chen Wang and Rohun Kulkarni and Li Fei-Fei and Silvio Savarese
          and Yuke Zhu and Roberto Mart'{i}n-Mart'{i}n},
  booktitle={arXiv preprint arXiv:2108.03298},
  year={2021}
}
```


## robomimic_ph/lift_low_dim (default config)

*   **Features**:

```python
FeaturesDict({
    '20_percent': tf.bool,
    '20_percent_train': tf.bool,
    '20_percent_valid': tf.bool,
    '50_percent': tf.bool,
    '50_percent_train': tf.bool,
    '50_percent_valid': tf.bool,
    'episode_id': tf.string,
    'horizon': tf.int32,
    'steps': Dataset({
        'action': Tensor(shape=(7,), dtype=tf.float64),
        'discount': tf.int32,
        'is_first': tf.bool,
        'is_last': tf.bool,
        'is_terminal': tf.bool,
        'observation': FeaturesDict({
            'object': Tensor(shape=(10,), dtype=tf.float64),
            'robot0_eef_pos': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_quat': Tensor(shape=(4,), dtype=tf.float64),
            'robot0_eef_vel_ang': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_vel_lin': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_gripper_qpos': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_gripper_qvel': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_joint_pos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_cos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_sin': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_vel': Tensor(shape=(7,), dtype=tf.float64),
        }),
        'reward': tf.float64,
        'states': Tensor(shape=(32,), dtype=tf.float64),
    }),
    'train': tf.bool,
    'valid': tf.bool,
})
```

## robomimic_ph/lift_image

*   **Features**:

```python
FeaturesDict({
    '20_percent': tf.bool,
    '20_percent_train': tf.bool,
    '20_percent_valid': tf.bool,
    '50_percent': tf.bool,
    '50_percent_train': tf.bool,
    '50_percent_valid': tf.bool,
    'episode_id': tf.string,
    'horizon': tf.int32,
    'steps': Dataset({
        'action': Tensor(shape=(7,), dtype=tf.float64),
        'discount': tf.int32,
        'is_first': tf.bool,
        'is_last': tf.bool,
        'is_terminal': tf.bool,
        'observation': FeaturesDict({
            'agentview_image': Image(shape=(84, 84, 3), dtype=tf.uint8),
            'object': Tensor(shape=(10,), dtype=tf.float64),
            'robot0_eef_pos': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_quat': Tensor(shape=(4,), dtype=tf.float64),
            'robot0_eef_vel_ang': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_vel_lin': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eye_in_hand_image': Image(shape=(84, 84, 3), dtype=tf.uint8),
            'robot0_gripper_qpos': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_gripper_qvel': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_joint_pos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_cos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_sin': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_vel': Tensor(shape=(7,), dtype=tf.float64),
        }),
        'reward': tf.float64,
        'states': Tensor(shape=(32,), dtype=tf.float64),
    }),
    'train': tf.bool,
    'valid': tf.bool,
})
```

## robomimic_ph/can_low_dim

*   **Features**:

```python
FeaturesDict({
    '20_percent': tf.bool,
    '20_percent_train': tf.bool,
    '20_percent_valid': tf.bool,
    '50_percent': tf.bool,
    '50_percent_train': tf.bool,
    '50_percent_valid': tf.bool,
    'episode_id': tf.string,
    'horizon': tf.int32,
    'steps': Dataset({
        'action': Tensor(shape=(7,), dtype=tf.float64),
        'discount': tf.int32,
        'is_first': tf.bool,
        'is_last': tf.bool,
        'is_terminal': tf.bool,
        'observation': FeaturesDict({
            'object': Tensor(shape=(14,), dtype=tf.float64),
            'robot0_eef_pos': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_quat': Tensor(shape=(4,), dtype=tf.float64),
            'robot0_eef_vel_ang': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_vel_lin': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_gripper_qpos': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_gripper_qvel': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_joint_pos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_cos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_sin': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_vel': Tensor(shape=(7,), dtype=tf.float64),
        }),
        'reward': tf.float64,
        'states': Tensor(shape=(71,), dtype=tf.float64),
    }),
    'train': tf.bool,
    'valid': tf.bool,
})
```

## robomimic_ph/can_image

*   **Features**:

```python
FeaturesDict({
    '20_percent': tf.bool,
    '20_percent_train': tf.bool,
    '20_percent_valid': tf.bool,
    '50_percent': tf.bool,
    '50_percent_train': tf.bool,
    '50_percent_valid': tf.bool,
    'episode_id': tf.string,
    'horizon': tf.int32,
    'steps': Dataset({
        'action': Tensor(shape=(7,), dtype=tf.float64),
        'discount': tf.int32,
        'is_first': tf.bool,
        'is_last': tf.bool,
        'is_terminal': tf.bool,
        'observation': FeaturesDict({
            'agentview_image': Image(shape=(84, 84, 3), dtype=tf.uint8),
            'object': Tensor(shape=(14,), dtype=tf.float64),
            'robot0_eef_pos': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_quat': Tensor(shape=(4,), dtype=tf.float64),
            'robot0_eef_vel_ang': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_vel_lin': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eye_in_hand_image': Image(shape=(84, 84, 3), dtype=tf.uint8),
            'robot0_gripper_qpos': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_gripper_qvel': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_joint_pos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_cos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_sin': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_vel': Tensor(shape=(7,), dtype=tf.float64),
        }),
        'reward': tf.float64,
        'states': Tensor(shape=(71,), dtype=tf.float64),
    }),
    'train': tf.bool,
    'valid': tf.bool,
})
```

## robomimic_ph/square_low_dim

*   **Features**:

```python
FeaturesDict({
    '20_percent': tf.bool,
    '20_percent_train': tf.bool,
    '20_percent_valid': tf.bool,
    '50_percent': tf.bool,
    '50_percent_train': tf.bool,
    '50_percent_valid': tf.bool,
    'episode_id': tf.string,
    'horizon': tf.int32,
    'steps': Dataset({
        'action': Tensor(shape=(7,), dtype=tf.float64),
        'discount': tf.int32,
        'is_first': tf.bool,
        'is_last': tf.bool,
        'is_terminal': tf.bool,
        'observation': FeaturesDict({
            'object': Tensor(shape=(14,), dtype=tf.float64),
            'robot0_eef_pos': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_quat': Tensor(shape=(4,), dtype=tf.float64),
            'robot0_eef_vel_ang': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_vel_lin': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_gripper_qpos': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_gripper_qvel': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_joint_pos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_cos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_sin': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_vel': Tensor(shape=(7,), dtype=tf.float64),
        }),
        'reward': tf.float64,
        'states': Tensor(shape=(45,), dtype=tf.float64),
    }),
    'train': tf.bool,
    'valid': tf.bool,
})
```

## robomimic_ph/square_image

*   **Features**:

```python
FeaturesDict({
    '20_percent': tf.bool,
    '20_percent_train': tf.bool,
    '20_percent_valid': tf.bool,
    '50_percent': tf.bool,
    '50_percent_train': tf.bool,
    '50_percent_valid': tf.bool,
    'episode_id': tf.string,
    'horizon': tf.int32,
    'steps': Dataset({
        'action': Tensor(shape=(7,), dtype=tf.float64),
        'discount': tf.int32,
        'is_first': tf.bool,
        'is_last': tf.bool,
        'is_terminal': tf.bool,
        'observation': FeaturesDict({
            'agentview_image': Image(shape=(84, 84, 3), dtype=tf.uint8),
            'object': Tensor(shape=(14,), dtype=tf.float64),
            'robot0_eef_pos': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_quat': Tensor(shape=(4,), dtype=tf.float64),
            'robot0_eef_vel_ang': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_vel_lin': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eye_in_hand_image': Image(shape=(84, 84, 3), dtype=tf.uint8),
            'robot0_gripper_qpos': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_gripper_qvel': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_joint_pos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_cos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_sin': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_vel': Tensor(shape=(7,), dtype=tf.float64),
        }),
        'reward': tf.float64,
        'states': Tensor(shape=(45,), dtype=tf.float64),
    }),
    'train': tf.bool,
    'valid': tf.bool,
})
```

## robomimic_ph/transport_low_dim

*   **Features**:

```python
FeaturesDict({
    '20_percent': tf.bool,
    '20_percent_train': tf.bool,
    '20_percent_valid': tf.bool,
    '50_percent': tf.bool,
    '50_percent_train': tf.bool,
    '50_percent_valid': tf.bool,
    'episode_id': tf.string,
    'horizon': tf.int32,
    'steps': Dataset({
        'action': Tensor(shape=(14,), dtype=tf.float64),
        'discount': tf.int32,
        'is_first': tf.bool,
        'is_last': tf.bool,
        'is_terminal': tf.bool,
        'observation': FeaturesDict({
            'object': Tensor(shape=(41,), dtype=tf.float64),
            'robot0_eef_pos': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_quat': Tensor(shape=(4,), dtype=tf.float64),
            'robot0_eef_vel_ang': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_vel_lin': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_gripper_qpos': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_gripper_qvel': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_joint_pos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_cos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_sin': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_vel': Tensor(shape=(7,), dtype=tf.float64),
            'robot1_eef_pos': Tensor(shape=(3,), dtype=tf.float64),
            'robot1_eef_quat': Tensor(shape=(4,), dtype=tf.float64),
            'robot1_eef_vel_ang': Tensor(shape=(3,), dtype=tf.float64),
            'robot1_eef_vel_lin': Tensor(shape=(3,), dtype=tf.float64),
            'robot1_gripper_qpos': Tensor(shape=(2,), dtype=tf.float64),
            'robot1_gripper_qvel': Tensor(shape=(2,), dtype=tf.float64),
            'robot1_joint_pos': Tensor(shape=(7,), dtype=tf.float64),
            'robot1_joint_pos_cos': Tensor(shape=(7,), dtype=tf.float64),
            'robot1_joint_pos_sin': Tensor(shape=(7,), dtype=tf.float64),
            'robot1_joint_vel': Tensor(shape=(7,), dtype=tf.float64),
        }),
        'reward': tf.float64,
        'states': Tensor(shape=(115,), dtype=tf.float64),
    }),
    'train': tf.bool,
    'valid': tf.bool,
})
```

## robomimic_ph/transport_image

*   **Features**:

```python
FeaturesDict({
    '20_percent': tf.bool,
    '20_percent_train': tf.bool,
    '20_percent_valid': tf.bool,
    '50_percent': tf.bool,
    '50_percent_train': tf.bool,
    '50_percent_valid': tf.bool,
    'episode_id': tf.string,
    'horizon': tf.int32,
    'steps': Dataset({
        'action': Tensor(shape=(14,), dtype=tf.float64),
        'discount': tf.int32,
        'is_first': tf.bool,
        'is_last': tf.bool,
        'is_terminal': tf.bool,
        'observation': FeaturesDict({
            'object': Tensor(shape=(41,), dtype=tf.float64),
            'robot0_eef_pos': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_quat': Tensor(shape=(4,), dtype=tf.float64),
            'robot0_eef_vel_ang': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_vel_lin': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eye_in_hand_image': Image(shape=(84, 84, 3), dtype=tf.uint8),
            'robot0_gripper_qpos': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_gripper_qvel': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_joint_pos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_cos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_sin': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_vel': Tensor(shape=(7,), dtype=tf.float64),
            'robot1_eef_pos': Tensor(shape=(3,), dtype=tf.float64),
            'robot1_eef_quat': Tensor(shape=(4,), dtype=tf.float64),
            'robot1_eef_vel_ang': Tensor(shape=(3,), dtype=tf.float64),
            'robot1_eef_vel_lin': Tensor(shape=(3,), dtype=tf.float64),
            'robot1_eye_in_hand_image': Image(shape=(84, 84, 3), dtype=tf.uint8),
            'robot1_gripper_qpos': Tensor(shape=(2,), dtype=tf.float64),
            'robot1_gripper_qvel': Tensor(shape=(2,), dtype=tf.float64),
            'robot1_joint_pos': Tensor(shape=(7,), dtype=tf.float64),
            'robot1_joint_pos_cos': Tensor(shape=(7,), dtype=tf.float64),
            'robot1_joint_pos_sin': Tensor(shape=(7,), dtype=tf.float64),
            'robot1_joint_vel': Tensor(shape=(7,), dtype=tf.float64),
            'shouldercamera0_image': Image(shape=(84, 84, 3), dtype=tf.uint8),
            'shouldercamera1_image': Image(shape=(84, 84, 3), dtype=tf.uint8),
        }),
        'reward': tf.float64,
        'states': Tensor(shape=(115,), dtype=tf.float64),
    }),
    'train': tf.bool,
    'valid': tf.bool,
})
```

## robomimic_ph/tool_hang_low_dim

*   **Features**:

```python
FeaturesDict({
    'episode_id': tf.string,
    'horizon': tf.int32,
    'steps': Dataset({
        'action': Tensor(shape=(7,), dtype=tf.float64),
        'discount': tf.int32,
        'is_first': tf.bool,
        'is_last': tf.bool,
        'is_terminal': tf.bool,
        'observation': FeaturesDict({
            'object': Tensor(shape=(44,), dtype=tf.float64),
            'robot0_eef_pos': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_quat': Tensor(shape=(4,), dtype=tf.float64),
            'robot0_eef_vel_ang': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_vel_lin': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_gripper_qpos': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_gripper_qvel': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_joint_pos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_cos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_sin': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_vel': Tensor(shape=(7,), dtype=tf.float64),
        }),
        'reward': tf.float64,
        'states': Tensor(shape=(58,), dtype=tf.float64),
    }),
    'train': tf.bool,
    'valid': tf.bool,
})
```

## robomimic_ph/tool_hang_image

*   **Features**:

```python
FeaturesDict({
    'episode_id': tf.string,
    'horizon': tf.int32,
    'steps': Dataset({
        'action': Tensor(shape=(7,), dtype=tf.float64),
        'discount': tf.int32,
        'is_first': tf.bool,
        'is_last': tf.bool,
        'is_terminal': tf.bool,
        'observation': FeaturesDict({
            'object': Tensor(shape=(44,), dtype=tf.float64),
            'robot0_eef_pos': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_quat': Tensor(shape=(4,), dtype=tf.float64),
            'robot0_eef_vel_ang': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eef_vel_lin': Tensor(shape=(3,), dtype=tf.float64),
            'robot0_eye_in_hand_image': Image(shape=(240, 240, 3), dtype=tf.uint8),
            'robot0_gripper_qpos': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_gripper_qvel': Tensor(shape=(2,), dtype=tf.float64),
            'robot0_joint_pos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_cos': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_pos_sin': Tensor(shape=(7,), dtype=tf.float64),
            'robot0_joint_vel': Tensor(shape=(7,), dtype=tf.float64),
            'sideview_image': Image(shape=(240, 240, 3), dtype=tf.uint8),
        }),
        'reward': tf.float64,
        'states': Tensor(shape=(58,), dtype=tf.float64),
    }),
    'train': tf.bool,
    'valid': tf.bool,
})
```